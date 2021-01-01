# Append-Metodu-Stack-ve-Heap-Mant-

urunler = ["Laptop" , "Mouse" , "Keyboard"]

print(urunler)
print(type(urunler))  

#appendin kullanımı: "urunler" listesine sonradan bir şey eklemek istiyorsak urunler.append yapıp ekleyeceğimiz ürünü vs. yazmak.

urunler.append("Telefon")
print(urunler)    #["Laptop" , "Mouse" , "Keyboard", "Telefon"]

#Bundan sonrası önemli , stack ve heap mantığı;

ogrenciler1 = ["İlker" , "Cavit" , "Berkay"]
ogrenciler2 = ["Kerem" , "Halil" , "Murat"]
                                             #Nesnel programlamaya şuan itibari ile girmiş oldun
ogrenciler1 = ogrenciler2 
ogrenciler2[0] = "Engin"      
print(ogrenciler1[0])    
print(ogrenciler1)
print(ogrenciler2) 
'''Aslında burada ogrenciler1 bellekte yok oluyor ve ogrenciler2 gibi davranıyor.
 Çünkü referans tipli olduğu için Heap özelliğinden yararlanılır,en kaba tabiriyle...
 Liste'nin bir referans numarası vardır ve eşitliğin diğer tarafındaki(ogrenciler1,ogrenciler2) o numaraya bakar.
 Daha sonra değer tip mantığı ile ogrenciler2'nin referans numarası ogrenciler1 ile aynı olur ve liste de aynı olur.
 Yani sonuç olarak: ogrenciler1["Engin" , "Halil" , "Murat"]
                    ogrenciler2["Engin" , "Halil" , "Murat"]
 Referans numarasına adres deniliyor,bellekteki adres.'''      

#Sonuçlar aynı. Burada değer ve referans tip dediğimiz durum söz konusu.

#Benzer bir örnek daha;

sayi1 = 10                        
sayi2 = 20

sayi1 = sayi2  #Burada sayi1 artık 20'dir. Bunu demek istiyor.Tamamen değerle ilgilenir.
sayi2 = 60     #sayi2 bariz 60'dır. 
print(sayi1)
print(sayi2)   


#Burada ise sayi2 ne ise sayi1'de o dur. Direkt eşitlenir,tamamen değere bakılır.
#sayi1'e bakılır sayi2 umursanmaz bile,yani sayi2'de değer ne varsa onu sayi1'e atar.



#Sonuç olarak; 
 # referans tip --> list(yani ogrenciler bölümü)
 # değer tip --> int(yani sayi1 ve sayi2, ikinci bölüm)

# referans tipler: class,listeler ve stringler'den oluşur. Yazı tabanlıdır. Olay Heap'de gerçekleşiyor.
# değer tipler: int,float,boolean(0,1) oluşur. Sayısal veri tabanlıdır. Olay Stack'de gerçekleşiyor.
