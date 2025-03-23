using System;

// Namespace ve Genişletilebilirlik Hakkında Açıklamalar
/*
   - Namespace, C# projelerinde kodları organize etmek için kullanılan bir yapıdır.
   - Farklı namespace’ler kullanmak, kodun daha okunabilir, modüler ve yönetilebilir olmasını sağlar.
   - Örneğin, büyük bir projede veritabanı işlemleri, kullanıcı işlemleri ve hesaplama işlemleri farklı namespace’lerde tanımlanarak düzen sağlanabilir.
   
   - Genişletilebilirlik , yazılımın zaman içinde yeni özellikler eklenmesine izin verecek şekilde tasarlanmasıdır.
   - Bu, modüler programlama, arayüzler ve bağımlılıkları minimize etme gibi yöntemlerle sağlanır.
*/

namespace MatematikIslemleri
{
    public class Hesaplama
    {
        public int Topla(int sayi1, int sayi2)
        {
            return sayi1 + sayi2;
        }

        public int Carp(int sayi1, int sayi2)
        {
            return sayi1 * sayi2;
        }
    }
}

namespace ProgramUygulamasi
{
    using MatematikIslemleri; 
    
    class Program
    {
        static void Main()
        {
            Hesaplama hesap = new Hesaplama();
            
            int toplam = hesap.Topla(10, 20);
            int carpim = hesap.Carp(5, 6);
            
            Console.WriteLine($"Toplam: {toplam}");
            Console.WriteLine($"Çarpım: {carpim}");
        }
    }
}

 
 
