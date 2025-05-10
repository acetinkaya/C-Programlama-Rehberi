# C Programlama Dili Rehberi

![alternatif metin](https://github.com/acetinkaya/C-Programlama-Rehberi/blob/main/kapak2.png)

Bu repo, C programlama dili üzerine hazırlanmış bir rehberdir. Temel konulardan ileri düzey uygulamalara kadar adım adım ilerleyen örneklerle, C programlama dilini öğrenme sürecinizi kolaylaştırmayı amaçlamaktayım.

🎯 Hedef Kitle

* C diline yeni başlayan öğrenciler

* C programlama dilini öğrenmek isteyen herkes

* Gömülü sistem uygulamalarında algoritma geliştirmeyi ve programlamaya ilgi duyan tüm geliştiriciler. 

# 📘 Ders Video İçerikleri:

C Programlama Dili Konu Anlatımı - 1 Videosu :> https://youtu.be/uJD-iz-rm0Q

C Programlama Dili Konu Anlatımı - 2 Videosu :> https://youtu.be/rb-bJ6QTJ0Q

Bilgisayarda Programlama C Dili Soru Çözüm Videosu :> https://youtu.be/KAMBb57Damw

# 📘 Ders İçerikleri:

## 1. C Programlama Diline Genel Bakış

- C Nedir?
  
-> Yüksek seviyeli, makine diline yakın, hızlı ve verimli bir programlama dilidir.

- C Programlama Dili Nerelerde Kullanılır?

-> İşletim sistemleri (Linux, Windows'un çekirdek işlem bölümleri), gömülü sistemler, algoritma geliştirme, donanım sürücüleri.

- Hangi C Derleyicisi Kullanılacaktır?

-> DevC++ Derleyicisinin "Dev-Cpp 5.11 TDM-GCC 4.9.2" versiyonu kullanılarak kodlar çalıştırılacaktır. 

![alternatif metin](https://github.com/acetinkaya/C-Programlama-Rehberi/blob/main/devc%2B%2B_1.png)

DevC++ "Dev-Cpp 5.11 TDM-GCC 4.9.2" sürümünü [SourceForge](https://sourceforge.net/projects/orwelldevcpp/) bağlantısından indirebilirsiniz.

![alternatif metin](https://github.com/acetinkaya/C-Programlama-Rehberi/blob/main/sourceforge_2.png)



•	İlk C Programı:

    #include <stdio.h>
    int main() 
    {
        printf("Merhaba Hayat\n");
        return 0;
    }

## 2. C Programlama Diline Giriş

2.1 Yorum Satırları

    // Tek satırlık yorum

    /*
      Çok satırlı
      yorum
    */

2.2 Değişkenler ve Veri Tipleri (int, float, double, char)
     
      int yas = 25;
      float sicaklik = 36.5;
      char harf = 'A';
      #define PI 3.14
      const int GUN_SAYISI = 7;

3. Operatörler

3.1 Aritmetik Operatörler

    int toplam = 5 + 3; // 8
    int carpim = 4 * 2; // 8

3.2 Karşılaştırma Operatörleri

    if (a == b) { printf("Esittir\n"); }

3.3 Mantıksal Operatörler
    
    if (a > 0 && b > 0) { printf("Pozitif sayilar\n"); }

    if (not1 >= 50 || not2 >= 50) { printf("Ders geçildi.\n"); }
    
    if (!aktif) { printf("Kullanıcı pasif.\n"); }

4. Kontrol Yapıları

4.1 Koşullu İfadeler
   
      if (yas > 18) 
      {
          printf("Yetiskin.\n");
      }
       else 
      {
          printf("Cocuk.\n");
      }

      ---

      int yas = 20;
      int puan = 85;
  
      if (yas >= 18 && puan >= 80) 
      {
          printf("Sınava girmeye uygunsunuz.\n");
      } 
      else 
      {
          printf("Şartları sağlamıyorsunuz.\n");
      }

      ---

4.2 switch-case Yapısı

    switch(gun)
    {
      case 1: printf("Pazartesi"); break;
      case 2: printf("Sali"); break;
      default: printf("Gecersiz gun");     
    }

4.3 Döngüler

4.3.1 for Döngüsü

    for(int i=0; i<5; i++) 
    {
        printf("%d\n", i);
    }

4.3.2 while Döngüsü

    int i = 0;
    while(i < 5)
    {
        printf("%d\n", i);
        i++;
    }

4.3.3 do-while Döngüsü

    int i = 0;
    do
    {
        printf("%d\n", i);
        i++;
    } while(i < 5);

5. Fonksiyonlar

5.1 Fonksiyon Tanımı ve Kullanımı

    int topla(int a, int b) 
    {
        return a + b;
    }
    
    int main()
     {
        int sonuc = topla(5, 3);
        printf("%d", sonuc);
    }

6. Diziler

6.1 Tek Boyutlu Dizi

    int sayilar[5] = {1, 2, 3, 4, 5};
    printf("%d", sayilar[2]); // 3

6.2 Çok Boyutlu Dizi

    int matris[2][3] = {{1,2,3}, {4,5,6}};
    printf("%d", matris[1][2]); // 6 

6.3 İşaretçiler - Pointers 
   
    int x = 42;            // Normal bir tamsayı değişkeni
    nt *p = &x;           // p, x'in adresini tutan gösterici

    printf("x  değeri : %d\n",  x);   // 42
    printf("&x adresi : %p\n", &x);   // Örn. 0x7ffd5c1e5b3c
    printf("p  adresi : %p\n",  p);   // Aynı adres → &x
    printf("*p değeri : %d\n", *p);   // 42   

7. C Programlama Dili Kütüphaneleri 

7.1. C Programlama Dilinde Genel Kullanımı Olan Kütüphaneler

| Başlık (header)   | Ana İşlev Grubu         | Sık Kullanılan Fonksiyonlar*  | Kısaca Ne Yapar   |    
|-------------------|---------------|--------------|----------------------------------------------------|     
| `<time.h>`        | Tarih & Zaman  | `time`, `localtime`, `gmtime`, `difftime`, `clock`, `strftime`   | Unix zaman damgası, yerel/zaman dilimi dönüşümü, süre ölçümü.  |
| `<stdio.h>`       | Girdi / Çıktı   | `printf`, `scanf`, `fprintf`, `fgets`, `fgetc`, `fputc`, `fseek`, `rewind` | Dosya ve ekran/klavye akışlarını biçimlendirilmiş olarak yönetir.    |
| `<stdlib.h>`      | Yardımcı & Bellek        | `malloc`, `calloc`, `realloc`, `free`, `atoi`, `atof`, `strtol`, `rand`, `srand`, `exit`, `system` | Dinamik bellek, sayı–metin dönüşümü, rastgele sayı, proses kontrolü.  |
| `<string.h>`      | Karakter Dizileri        | `strlen`, `strcpy`, `strncpy`, `strcat`, `strcmp`, `strchr`, `strstr`, `memset`, `memcpy`, `memmove` | C-string işlemleri ve ham bellek kopyalama/doldurma.  | 
| `<math.h>`        | Matematik  | `sqrt`, `pow`, `sin`, `cos`, `tan`, `log`, `exp`, `fabs`, `ceil`, `floor` | Karekök, trigonometrik, logaritmik ve yuvarlama fonksiyonları. 

7.2. C Programlama Dilinde Özel Kullanımı Olan Kütüphaneler

| Başlık (header)   | Ana İşlev Grubu         | Sık Kullanılan Fonksiyonlar*                                    | Kısaca Ne Yapar                                                                 |
|-------------------|--------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `<ctype.h>`       | Karakter Sınıflama       | `isalnum`, `isalpha`, `isdigit`, `isspace`, `tolower`, `toupper`                | Karakter türünü sınar veya harfi büyük/küçük yapar.                             |
| `<assert.h>`      | Hata Ayıklama            | `assert`                                                                         | Koşul sağlanmazsa çalışma anında mesaj basıp programı sonlandırır.              |
| `<signal.h>`      | Sinyal İşleme            | `signal`, `raise`, `kill`                                                        | Çeşitli “sinyal” olaylarını yakalamak veya tetiklemek için (örn. `SIGINT`).     |
| `<errno.h>`       | Hata Kodları             | `errno` (makro), `perror`, `strerror`                                            | Sistem çağrılarında oluşan hataları standart kod/mesaja çevirir.                |
| `<locale.h>`      | Yerelleştirme            | `setlocale`, `localeconv`                                                        | Ondalık ayraç, para birimi, alfabetik sıralama vb. kültür ayarlarını yönetir.   

8. C Programlama Dili Örnekleri

8.1. Kullanıcı Girdisinin Doğruluğunu scanf() ile Kontrol Etme

    #include <stdio.h>
    
    int main()
    {
    int sayi = 0;
    int sonuc = 0;
    
    printf("Bir sayi girin: ");
    
    sonuc = scanf("%d", &sayi);
    
        if (sonuc == 1) 
        {
            printf("Girilen sayi: %d\n", sayi);
        } 
        else 
        {
            printf("Gecersiz karakter girisi yaptiniz.\n");
        }
    
    }

8.2. Girilen Bir Sayının Tek mi Çift mi Olduğunu Bulma

    #include <stdio.h>
    
    int main()
    {
        int sayi;
    
        printf("Bir sayı girin: ");
        scanf("%d", &sayi);
        
        if (sayi % 2 == 0) 
        {
            printf("%d çift sayıdır.\n", sayi);
        } 
        else 
        {
            printf("%d tek sayıdır.\n", sayi);
        }  

    }

8.3. Girilen Bir Değerin Sayı Olduğu Kontrol Edildikten Sonra Tek mi Çift mi Olduğunu Bulma

    #include <stdio.h>
    
    int main()
    {
        int sayi = 0;
        int sonuc;
        
        printf("Bir sayı girin: ");
        sonuc = scanf("%d", &sayi);
    
        if (sonuc == 1) 
        {
            if (sayi % 2 == 0) 
            {
                printf("%d çift sayıdır.\n", sayi);
            } 
            else 
            {
                printf("%d tek sayıdır.\n", sayi);
            }
        } 
        else 
        {
            printf("Geçersiz giriş! Lütfen bir tamsayı giriniz.\n");
        }
    
    }

8.4. Kullanıcıdan Alınan Sayıları Diziye Aktarma ve Yazdırma

    #include <stdio.h>
    
    int main() 
    {
        int sayilar[6];
        int i;
    
        // Kullanıcıdan 6 sayı alınıyor...
        printf("Lutfen 6 adet tamsayı giriniz:\n");
        for (i = 0; i < 6; i++) 
    	  {
            printf("%d. sayi: ", i + 1);
            scanf("%d", &sayilar[i]);
        }
        
        // Girilen sayıları yazdır
        printf("\nGirilen sayilar:\n");
        for (i = 0; i < 6; i++) 
    	  {
            printf("%d ", sayilar[i]);
        }
    }


8.5. Kullanıcıdan Alınan Sayıların Ortalamasını Hesaplama

    #include <stdio.h>
    int main() 
    {
        int sayilar[6];
        int i, toplam = 0;
        float ortalama;
        printf("Lütfen 6 adet tamsayı giriniz:\n");

        for (i = 0; i < 6; i++) 
    	  {
            printf("%d. sayi: ", i + 1);
            scanf("%d", &sayilar[i]);
            toplam += sayilar[i];
        }
    
        ortalama = (float)toplam / 6;
    
        printf("\nGirilen sayıların ortalaması: %.2f\n", ortalama);
    
    }

8.6. Kullanıcıdan Alınan Sayıların Diziye Atılması ve Tek–Çift Sayıların Adetlerinin Belirlenmesi

    #include <stdio.h>
    
    int main() 
    {
        int sayilar[6];
        int i, tekSayac = 0, ciftSayac = 0;
    
        printf("Lütfen 6 adet tamsayı giriniz:\n");
        for (i = 0; i < 6; i++) 
    	  {
            printf("%d. sayi: ", i + 1);
            scanf("%d", &sayilar[i]);
    
            if (sayilar[i] % 2 == 0)
                ciftSayac++;
            else
                tekSayac++;
        }
        
        printf("\nGirilen sayılar arasında:\n");
        printf("Tek sayı adedi: %d\n", tekSayac);
        printf("Çift sayı adedi: %d\n", ciftSayac);
    
    }

8.7. Örnekler devam edecektir....


----

## 📖 Kaynak Kitaplar

1. Harvey M. Deithel, Paul J. Deitel,  "C ve C++", Sistem Yayıncılık, İstanbul, 2011.

2. Prof. Dr. Ercan Nurcan Yılmaz, Dr. Serkan Gönen, "Örneklerle Uygulamalı C ve C++", İstanbul Gelişim Üniversitesi Yayınları, İstanbul, 2023.

3. Nergiz Ercil Çağıltay, Gül Tokdemir, C. Fügen Selbes, Çiğdem Turhan, "C Dersi Programlamaya Giriş", Kişisel Yayınlar, Ankara, 2010.

4. Nergiz Ercil Çağıltay, Gül Tokdemir, C. Fügen Selbes, Çiğdem Turhan, "C Dersi Çözümlü Problem Kitabı", Ankara, 2012.

5. Dr. Erdal Güvenoğlu, "Çözümlü C Örnekleri", Nobel Akademik Yayıncılık, Ankara, 2022.

6. Prof. Dr. Fatih Başçiftçi, "C Programlama Dİli", Atlas Akademi, Konya, 2010.

7. C. Laplace and

⚡ **Bilgi Paylaştıkça Gelişir!** 🚀 

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Bu Github paylaşımının IEEE ve APA formatlarınada atıf verilme şekli:

IEEE--> A. Cetinkaya, "C Programlama Dili Rehberi" GitHub, [Online]. Erişim Linki: https://github.com/acetinkaya/C-Programlama-Rehberi. Son Erişim Tarihi: Gün Ay Yıl.

APA--> Cetinkaya, A. (2025). C Programlama Dili Rehberi [GitHub Deposu]. GitHub. Erişim Linki: https://github.com/acetinkaya/C-Programlama-Rehberi. Son Erişim Tarihi: Gün Ay Yıl.

---

Yukarıdaki bilgi, resim ve kod çalışmaları açık kaynak paylaşım olarak GitHub "acetinkaya" alanında paylaşımı yapılmıştır.

Proje Durumu: İlgili paylaşımlar ve C programlama dilinde yazılmış yazılım kodlarına sürüm güncellemeleri yaptıkça bu paylaşımları güncelleyeceğiz. GitHub bölümünden beğeni bildirimi olarak bir yıldız vererek çalışmalarımı destekleyebilirsiniz. Bilgi paylaşıldıkça büyür ve gelişir.

Katkıda Bulunma: Fork - Çekme istekleri memnuniyetle karşılanır. Büyük değişiklikler için lütfen önce neyi değiştirmek istediğinizi görüşmek üzere ilgili C kodunu belirttiğiniz bir soru - yanıt bölümü açın. 
Bilgi paylaşıldıkça çoğalır ve gelişir. İyi çalışmalar dilerim.

Yazar ve Güncelleme Yapan: [Öğr. Gör. Ali Çetinkaya (MSc.)](https://github.com/acetinkaya) - 2025

---

The above information, images, and code examples are shared as open-source content on GitHub under the "acetinkaya" account.

Project Status: The relevant posts and software codes written in the C programming language will be updated as new versions are released. You can support my work by giving a star to the repository on GitHub. Knowledge grows and develops as it is shared.
Contributing: Forks and pull requests are warmly welcomed. For major changes, please first open a question-answer thread indicating which C code you want to modify to discuss your proposal. Knowledge multiplies and improves when shared. Best wishes for your work!

Author and Maintainer: [Lect. Ali Cetinkaya (MSc.)](https://github.com/acetinkaya) - 2025

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
