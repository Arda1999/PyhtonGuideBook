# PyhtonGuideBook
Veri Tipleri Islemler
22.7 // 11.4   Bu bolumunden kalani al demek
2**4  16 demek yani ussunu almaktır.
4 % 2  Bolumunden kalani al demektir.
				           Stringler
“””” mernaha “”””  Stringler 3 farkli skilde olsuturulur.
“merhaba ”
‘ merhaba ‘

a = “ pyhton programlama dili”
a[4:10(dahil değil)] demek 4. İndeksten basla 10 indeks dahil değil ama al
a[:10]  10. İndekse kadar al demek ama 10 dahil degil.
a[4:10:2]  ikişer ikişer atlayarak 4. İndeksten basla 10.indekse kadar al.
a[::-1]  bastan sonra 1 atlayarak strignleri al.
Len(a) ile stringin uzunluğunu buluruz.

A =’ arda’
B = ‘peker’
C = ‘naber’
A + B+ C  arda peker naber






Global ve Local Variables
	Fonksiyon içinde tanimlanan degiskenler yerel degiskenlerdir yani fonskiyonun disinda tanimlaninca yok olur.
	Global degiskenler ise fonksiyonlarin disina tanimlanirlar ve programin her yerinden ulaşabiliriz.
	
b= 10 #global variabledir.
def fonksiyon(a): 
    a = 10 #local variabledir.
    print(a)
    print(b)#global degisken oldugu icin buradanda ulasiriz.
    
fonksiyon()
print(a) # a degiskeni yok oldu
print(b)  # global degisken oldugu icin buradanda ulasiriz.






	






Veri Tipi Donusumleri
a = 43
float(a) #float a donusturduk

b = 43.1
int(a) #integere donusturme

a =3321321
str(a) # a sayisi stringe donustu
	
Print ve Formatlama
\n  alt satira geçer
\t  boşluk birakir
Print(“a \n b”)
Print(“a \t b”)

a = 45
print(type(a)  ile biz a nin hangi tur de olduğunu anlarirz

print(34,12,42,15)
# output = 34 12 42 15
print(34,12,45,12,sep='/')
#output = 24/12/45/12
print(34,12,45,12,sep='\n')
#34
#12
#45
#12

Formatlama
a =45
b ="arda"
print("{}'nin {} numarasi ".format(a,b))

print("{1} {0} {2}".format(43,"Murat",54))  Murat 43 54


Listeler
liste = [] # Bos liste
liste = list() # Bos liste
liste1 = [1,2,'elma',3,4]
len(liste1) #liste1 in uzunlugunu bulduk.
liste1[1] # listenin 1.elemani
liste1[:3] # Bastan 3. indekse kadar al
liste1[-1] #sonuncu elemani alir.

liste1 =[1,3,4]
liste2 =[4,5,2]
liste1 + liste2 # 1,3,4,4,5,2


liste = [1,2,3,4,4,4]
liste.pop()#sonuncu elemani cikarir
liste.pop(3)#3.elemani cikarir.
liste.append(5)#listeye 5 ekler
liste.sort()#listeyi kucukten buyuye siralar.
liste.sort(reverse=True)#listeyi buyukten kucuge siralar.
Liste.insert(1,”java”) ile listenin hangi indeksine ekleyeceksek onu veririrz.
Liste.remove(1) dersek 1 elemanini listeden siler.
Liste.index(2,4) dersek iki değerini 4.indexten itibaren ariyoruz demek.
Liste.index(2) dersek iki elemaninin indexini dondurur.
Liste.count(4) 4 elemaninin listede kac kez donduğunu söyler.
Liste.sort() ile listeyi küçükten buyuge dogru dizer.
					
liste = [1,2,3,4,5]
liste = [i * 2 for i in liste]
print(liste)  2,4,6,8,10

Liste = [1,2,3,4,5]
     Liste.insert(1,”murat”)

NumPy  Listelere gore 50 kat daha hizli bir dizi nesnesi oluşturur.


List Comphression
liste_1 = [1,2,3,4,5]
liste_2 = [i for i in liste_1]

print(liste_2)

>>> [1,2,3,4,5]
Veya
liste_1 = [[1,2,3],[4,5,6],[7,8,9]]

liste_2 = [x for i in liste_1 for x in i]

print(liste_2)
>> 1 2 3 4 5 6 7 8 9
Veya
list1 = ["Hello ", "take "]
list2 = ["Dear", "Sir"]
res = [x + y for x in list1 for y in list2]
print(res)
Bu kodun asil hali;

list1 = ["Hello ", "take "]
list2 = ["Dear", "Sir"]
for x in list1:
	for y in list2:
		res = x+y
print(res)
	
OUTPUT HELLO DEAR HELLO SIR TAKE DEAR TAKE SIR





Demetler(TUPLES)
# demetler elemanlari parantez icinde alarak olsuturulur.
#DEMETLERDEKI ELEMANLAR DEGISTIRIELEMEZLER VE SILINEMEZLER

demet = (1,2,3,4,5)
demet[1] # 1. elemana ulasiriz.

demet = (1,1,1,1,1,3)
demet.count(1) # demetteki 1 leri sayar.

demet = ("arda","peker","akilli")
demet.index("peker")# demetteki indeksini yani 1 dondurur.



Dictonary

sozluk = {} #Bos sozluk
sozluk = dict() # Bos sozluk

a = {"sifir":0,"bir":1,"iki":2}
a["iki"]#output 2 cikar
a.keys()# output sifir bir iki doner.
a.values() #output 0 1 2 doner
a.items() #butun degerler doner.

Kullanicidan Input Alma

a = input("lutfen sayi giriniz")
print("kullanicinin girdigi sayi {}".format(a))

#Kullanicidan integer bir deger almak icin deger donusumu yapmamiz lazim
#yani integere cevirmemiz lazim cunku input lininca string aliniyor.
a = int(input("bir sayi giriniz"))
print("girilen deger {}".format(a))

Donguler
==  !=    >=     <=     >     <
1 < 2 and "arda " == "arda"

1 < 2 or "arda" == "arda"

not 1>2

if(yas == 12):
    print("kucuk")
elif(yas == 145):
    print("buyuk")
else:
    print("ortanca")



For Dongusu
liste = [1,3,4,5]
for i in liste:
    print("{}".format(i))

s = 'arda'
for i in s:
    print(i)

liste = [(1,3),(3,1),(5,6)]
for (i,j) in liste:
    print("i:{} j:{}".format(i,j))  i 1 j 3
					i 3 j 1
					i 5 j 6
While Dongusu
liste = [1,2,3,4,5,6,7]

index = 0;
while(index < len(liste)):
    print("index",index,"liste elemani",liste[index])
    index = index +1
Range
print(*range(1,20)) // 1,2,3,4,5,6,7,8,9,10,..,20
print(range(1,20) // 1,20
for i in range(100): // bu da 0’dan 100’e kadar sayi uret demek.

Breake/Continue
i = 0
while(i<10):
    if(i == 5):
        break;
    print(i)
    i = i +1  1 2 3 4 

liste = list(range(10))
for i in liste:
    if(i==3 or i == 5):
        continue // buradan sonra direk blogun basina doner.
    print(i)  0,1,2,4,6,7,8,9,10

Fonksiyonlar
def faktoriyel(sayi):
    faktoriyel=1
    if(sayi == 0 or sayi == 1):
        print("Faktoriyel",faktoriyel)
    else:
        while(sayi >= 1):
            faktoriyel = faktoriyel * sayi
            sayi = sayi - 1

        print("faktoriyel",faktoriyel)


def toplama(a,b):
    return a + b

toplama(4,5)
def ikiylecarp(c):
    return c * 2
ikiylecarp(5)  

def bilgigoster(ad ="bilgiyok",soyad = "bilgiyok"):
    print("ad:",ad, "soyad:",soyad)

bilgigoster() # ad: bilgiyok soyad: bilgiyok
bilgigoster("arda","peker") # ad: arda soyad: peker 


Lambda ile Fonksiyon Tanimlama
def cifttek(sayi):
    return sayi % 2 == 0             cifttek = lambda sayi: sayi % 2 == 0

	Yukaridaki fonksyonun lambda ile tanimlanmasi.


Ic Ice Fonksıyonlar
def fonksiyon(*args):
#args ile fonksiona birden fazla parametre gonderebiliyorz.
    for i in args:
        print(i);

fonksiyon(1,2,3)

#Bir fonksiyona birden fazla string deger yollamak istersek kullaniriz.
def fonksiyon(**kwargs):
    
    print(kwargs)

fonksiyon('isim:''murat','soyisim:''peker');

def fonksiyon(*args,**kwargs):
    for i in args:
        print(i)
        
    for i,j in kwargs.items():
        print(i,j)
    

fonksiyon(1,2,3,4,5,'isim:''murat','soyisim:''peker');

def fonksiyon():
    def fonksiyon2():
        print("kucuk fonskiyondan herkese merhaba");
    fonksiyon2()
    print("buyuk fonskiyondan herkese merhaba");

fonksiyon()



Return ile Fonksiyon Donmek

def fonksiyon(islem_adi):
    def toplama(*args):
        toplam = 0
        for i in args:
            toplam += i
        return toplam
    def carpim(*args):
        carpim = 1
        for i in args:
            carpim*=i
        return  carpim
    if islem_adi == toplama:
        return toplama
    else:
        return carpim
fonk = fonksiyon("toplama")
fonk(1,2,3,4)

def toplama(a,b):
    return a+b
def cikarma(a,b):
    return a-b
def carpma(a,b):
    return a*b
def bolme(a,b):
    return a/b

def anafonkiyon(func1,func2,func3,func4,islem_adi):
    if islem_adi == "toplama":
        print(func1(3,4))
    elif islem_adi =="cikarma":
        print(func2(5,2))
    elif islem_adi =="carpma":
        print(func3(6,3))
    else:
        print(6,2)
anafonkiyon(toplama,cikarma,carpma,bolme,"toplama")



Decorator Tekrarli Fonskiyonlar 
Buradaki olay eger iki fonksiyonda ayni seyleri kullanacaksa bunlari bir wrapper fonskiyonunda toplayip daha sonrasinda bunlari fonksiyonlardan once @ işareti ile cagirirsak otomatik olarak fonksiyonlara tanimlanmis olacaklardır veya fonksiona eksra ozlellik eklersek
ORNEGIN:
#decorator fonksiyon tanimlama amaç ortalama bul fonskiyonuna ekstardan hem cift sayilarin hem de tek sayilarin ortalamasini buldurmak.
def ekstra(fonk):
    #wrapper diye fonk tanimlamaliyiz.
    def wrapper(sayilar):#Asagida ortalama bul fonksiyonundaki sayilar listesini buraya atiyoruz.
        ciftlertoplami= 0
        cift_sayilar = 0
        tek_sayilar = 0
        teklertoplami=0
        for sayi in sayilar:
            if(sayi % 2 == 0):
                ciftlertoplami += sayi
                cift_sayilar += 1
            else:
                teklertoplami += sayi
                tek_sayilar += 1

        print("teklerin ortalamsi {}".format((teklertoplami/tek_sayilar)))
        print("ciftleri ortalamsi {}".format((ciftlertoplami/cift_sayilar)))
        fonk(sayilar)
        return wrapper()

#decorator fonksiyonu cagirmak icin @ isaretini kullancaz
@ekstra
def ortalama_bul(sayilar):
    toplam = 0
    for sayi in sayilar:
        toplam+=sayi
    print("Genel ortalama:",toplam/len(sayilar))
print(ortalama_bul(1,2,3,4,5))

Pyhtondaki Ileri Seviye Moduller
Os Modulu = Dosyalarda kolaylikla islem yapmamizi saglayan hazir moduldur(silme ekleme gibi).
import os

print(dir(os))#os modulu icindeki modulleri gorebiliriz.
print(os.getcwd())# olusturudum dosyanin yolunu gosterir.
print(os.listdir()) #ile su anda bulundugumuz dosyanin altindaki dosyalari listeler.
print(os.mkdir("deneme"))#su anki klasorde yeni directory olusturur.
print(os.rmdir("deneme"))#deneme klasorunu sileriz.
print(os.rename("deneme.txt","deneme2.txt"))# deneme dosyasinin ismini deneme2 olarak degistirdik.
Sys Modulu = Kullanilan pyhton surumu ile ilgili bilgi edinmemizi saglar.
import sys

a = int(input("a:"))
b = int(input("b:"))
sys.exit()# bunu dedikten sonra asagidaki calismaz, program sonlanir.
c = int(input("c:"))

Pyhton Pip uygulama geliştirirken paketleri indirmek için kullaniriz npm gibi bir sey








Internetten veri cekme ve parçalama Request ve BeautifulSoup Modulleri
 

import requests
from bs4 import BeautifulSoup
url = "https://yellowpages.com.tr/"
response = requests.get(url)
print(response)
html_icerigi = response.content
soup = BeautifulSoup(html_icerigi,"html.parser")
print(soup.prettify())

#burada html kodlarindan a etiketine sahip olanlari dondurduk.
for i in soup.find_all("a"):
    #a etiketi altindaki sadece href ozelligine sahipleri aldik yani url leri aldik.
    print(i.get("href"))
    print(i)

#Class ismi belirli olan divleri almak istersek
print(soup.find_all("div",{"class":"yp-poi-box-2"}))

!!! BeautifulSoup ile internetten verileri pyhton ile çekebiliriz. !!!


Imdb top 250 olan filmleri cekelim internetten
import requests
from  bs4 import BeautifulSoup

url = "http://www.imdb.com/chart/top"

response = requests.get(url)

html_icerigi = response.content

soup = BeautifulSoup(html_icerigi,"html.parser")

basliklar=  soup.find_all("td",{"class":"titleColumn"})
ratingler = soup.find_all("td",{"class":"ratingColumn imdbRating"});

#zip fonksiyonu bize liste veya demet gibibir yapi olusturuyordu ve burada birinci elemanimiz baslik olucak ikinic elemaninimz ratingler olucak.
for baslik,rating in zip(basliklar,ratingler):
    baslik = baslik.strip()
    baslik = baslik.replace("\n","")

    rating = rating.strip()
    rating = rating.replace("\n","")

    print("Baslik",baslik.text)
    print("Rating",rating.text)

PILLOW ile fotoğraflar uzerinde islem yapma
pip3 install Pillow ile indiriyoruz.
 












Moduller

Her dosya bir moduldur ve bu modülleri projelere dahil ederek programlari daha hizli yazariz.
import math #math modulunu programa dahil ettik
#import math as matekatik bu sayede math modulunu matematik olarak kullaniriz.
dir(math)#dir ve modul ismi ile biz modulde neler var goruruz.
math.factorial(5)# otomatik olarak direk faktoriyeli aliriz.
math.floor(5.6)
math.ceil(4.1)

from math import * #math modulundeki her seyi dahil etmek icin.
factorial(5) # bu yontemle modul ismini yazmya gerek kalmadi.

KENDI MODULUMUZU YAZALIM.
-1 MASAUSTUNDE KLASOR OLUSTUR.
-2KLASORUN ICINDE IKI ADET .PY UZANTILI TEXFILE OLUSTUR.
 
Burada solda modül1 diye bir modul tanimladik ve modulun içine kendimiz olusturdugumuz fonksyionlari yazdik daha sonra sagda deneme diye bir dosya oluşturduk ve import modul1 diye cagirdik ve yazdigimiz modüldeki fonksiyonlara ulastik.
import random
import time

print("1 ile 40 arasinda sayi tahmini")

rastgele_sayi = random.randint(1,40)
tahmin_hakki = 7

while (tahmin_hakki != 0):
    tahmin = int(input("Tahmin:"))
    if(tahmin <rastgele_sayi):
        print("bilgiler sorgulaniyor")
        time.sleep(1)
        tahmin_hakki = tahmin_hakki-1
        print("daha yuksek sayi gir.")
    elif(tahmin > rastgele_sayi):
        print("bilgiler sorgulaniyor")
        time.sleep(1)
        tahmin_hakki = tahmin_hakki - 1
        print("daha dusuk sayi gir.")
    else:
        print("dogru bildiniz")

CLASSLAR

class Araba():
    model = "reno"
    renk = "gumus"
    beygir = 110
    
araba1 = Araba()

print(araba1.model,araba1.renk,araba1.beygir)


class Araba():
    def __init__(self,model,renk,beygir):=> classda ilk tanimlanan fonskiyondur ve self ismi zorunlu değil başka bir sey de yazabiliriz ama asil amaç classin içindeki verilere ulaşmak.
        self.model = model
        self.renk = renk
        self.beygir = beygir


araba1 = Araba("reno","gumus",110)

print(araba1.renk,araba1.model,araba1.beygir)

#classa methodlar eklemek
class Yazilimci():
    def __init__(self,isim,soyisim,maas):
        self.isim = isim
        self.soyisim = soyisim
        self.maas = maas
    def bilgileriGoster(self):
        print("yazilimci objesinin ozellikleri"
              "isim {}"
              "soyisim {}"
              "maas {}".format(self.isim,self.soyisim,self.maas))
    def zamyapiliyor(self,zam_miktari):
        self.zam_miktari = zam_miktari
        self.maas = self.maas +self.zam_miktari
yazilimci1 = Yazilimci("arda","peker",16000)

#yazilan bilgileri gostermek icin
yazilimci1.bilgileriGoster()

yazilimci1.zam_miktari(1000)

					Kalitim
class Calisan():
    def __init__(self,isim,maas,departman):
        self.isim = isim
        self.maas = maas
        self.departman = departman
    def bilgilerigoster(self):
        print("isim{}\n maas{} \n departman{}".format(self.isim,self.maas,self.departman))
    def departmandegistir(self,yeni_dep):
        self.departman= self.yeni_dep

#olusturucagimiz yonetici sinifi calisan sinifindan miras alicak
class Yonetici(Calisan):
    pass#sonradan bir sey tanimlamak icin kullanilir.
yonetici1 =Yonetici("arda",1000,"bilgisayar")

yonetici1.bilgilerigoster()
yonetici1.departmandegistir("tip")

#ust classin elemanlarina ulastik.
					
Override
class Calisan():
    def __init__(self,isim,maas,departman):
        self.isim = isim
        self.maas = maas
        self.departman = departman
    def bilgilerigoster(self):
        print("isim{}\n maas{} \n departman{}".format(self.isim,self.maas,self.departman))
    def departmandegistir(self,yeni_dep):
        self.departman= self.yeni_dep

#olusturucagimiz yonetici sinifi calisan sinifindan miras alicak
class Yonetici(Calisan):
    #yukaridaki init in uzerine kisi sayisi yazdik yani override ettik.
    def __init__(self, isim, maas, departman,kisisayisi):
    
     super().__init__(isim,maas,departman)

     self.kisisayisi = kisisayisi

   def zamyapiliyor(self,zam):
       self.maas = self.maas + zam
yonetici1 = Yonetici("arda",1000,"yonetici",10)
					


Class Ozel Methodlari
class Kitap():
    def __init__(self,isim,yazar,sayfa):
        self.isim =isim
        self.yazar = yazar
        self.sayfa = sayfa
    def __str__(self):#str string deger dondurur geriye
        return "isim{} \n yazar{} \n sayfa sayisi{}".format(self.isim,self.yazar,self.sayfa)
    def __len__(self):#sayi degerini geriye dondurur
        return self.sayfa
    def __del__(self):#obje silmek icin kullaniriz.
        pass

        
kitap1 = Kitap("arda","ahmet",100)
del kitap1 #kitap1 objesini sildik.		
Pyhton Yineyeliciler
Teknik olarak Python'da yineleyici, __iter__() ve __next__()






				Try Catch
try:
    a = int(input("sayi1"))
    b = int(input("sayi2"))
    print(a/b)
except ValueError:
    print("lutfen inputu dogru giriniz")
except ZeroDivisionError:
    print("Sayi 0 a bolunmez")
finally:
    print("Try Catch bitti")
    

				Gomulu Fonksiyonlar
#MAP fonksiyonu for listeye benzer bir objedir ve for dongusunu benzer

def fonk(x):
    return x * 2

list(map(fonk,[1,2,3,4]))#donen degerleri listeye atadik.
#map fonskiyonu ile fonk adindaki fonskiyona 1 2 3 4'u teker teker atiyoruz

				


#REDUCE, map fonksiyonundaki gibi ilkten fonksiyonun isimi sonrada yanina parametreleri tanimliyoruz.
#reucenin mantigi ilkten ilk iki elemana uyguluyor sonra cikan degeri ucuncu elemana uygular diye gider.
from functools import reduce
def toplama(x,y):
    return x + y
reduce(toplama,[12,31,42,12])

#FILTER reduceye cok benzer fonksiyon ve liste aliyor.
#amac sadece listedeki true olan degerleri dondurur.

filter(lambda x:x%2 ==0,[1,2,3,4,5,6,7])
#2,4,6









#ZIP fonksiyonu listelerin elemanlarini birletirir.

 














#ENUMARATE ile biz elemanlari numaralandiririz.

 
 
				 Ileri Seviye Sayilar
	Bin(4) ile sayiyi ikilik tabana cevririz. 0b100 demek 0b demek binary olduğunu söyler.
	Hex(300) ile sayiyi 16lik tabana çeviririz. 0x12c demek 0x demek hexadecimal oldgunu gösterir.
	Abs(-5) sayiyin mutlak değerini alir.
	Round(4.5) ile sayiyi asagiya yani 4 e yuvarlariz.
	Max(3,4,5,2) ile sayilardan en buyugunu dondururuz.
	Min(3,4,5,2) ile sayilardan en kucugunu dondururuz.
	Sum(3,1,2,3,6) ile sayilarin toplandigi değeri dondururuz.
	Pow(2,4) ile 2 uzeri 4 diyoruz.
	“pyhton”.upper() ile değerleri buyuk harf yapariz.
	“PYHON”.lower() ile değerleri kucuk harf yapariz.
	“Herkes ana baci kardas”.replace(“a”,”o”) ile a ile o karakterlerini değiştiririz.
	“Pyhton”.startswith(“P”) True değerini dondurur.
	Liste = “arda-peker-kocsistem”.split(“-”)  arda,peker,kocsistem
	“                                    Arda                                   “.strip() ile bosluklari sileriz ve sonuç sadece boşluksuz sekilde Arda cikar.
	Liste = [“T”,”B”,”M”,”M”]
“.”.join(liste)  T.B.M.M
	“ada kapisi yandan arkli”.count(“a”) ile cümledeki a lari sayariz.
	“araba”.find(“a”) ile indeksin içinde soldan baslar ve ilk bulduğu a değerini dondurur bulamazsa -1 dondurur.
SET
x = {1,2,3}#Kumeler suslu parantez ile tanimlanir.
liste = [1,1,1,1,2,2,2,3,3,3]
x = set(liste)# dersek listeyi kumeye donustururz ve sonuc 1,2,3 cikar her degerden bir tane yazar.
x.add(6) ile kümeye yeni eleman ekleriz.
x.discard(1) ile kümeden eleman cikaririz.

	Py uzantili ve Pyc uzantili dosya farki
Py Pyhton programlama dosyasiyken, pyc virtual machinenin okuyabilmesi için derleren dosyadır.














Iteratorler
Teknik olarak Python'da yineleyici, __iter__() ve __next__()
Iteratorler uzerinde gezinebilecek objelerdir ve bu objeler tek eleman dondururler.
İter() fonk. Kullanicaz ve bi sonraki elemani almak için next() kullancaz.
liste = [1,2,3,4]
iterator = iter(liste)
print(next(iterator))//1
print(next(iterator))//2 diye listenin elemanlarina ulasiriz.

Kendi itarable objemizi olusturmak için __iter()__ ve __next()__ fonksiyonlarina ihtiyacimiz var.
class Kumanda():
    def __init__(self,kanal_listesi):
        self.kanal_listesi =kanal_listesi;
        self.index = -1
    def __iter__(self):
        return self;
    def __next__(self):
        self.index +=1;
        if (self.index < self.kanal_listesi):
            return self.kanal_listesi[self.index]
        else:
            self.index = -1
            raise StopIteration #Raise ile try catch kullanmadan kullaniciya StopIteration hatasini bildirdirdik.Butun liste next ile bittikten sonra hata vermesi icin

kumanda = Kumanda(['ATV','TRT','FOX'])# obje olusturduk.
iterator = iter(kumanda)
next(iterator)

class Sayilarim(): 
def __iter__(self):
 self.a = 1 
return self 
def __next__(self): 
if self.a <= 20: 
x = self.a 
self.a += 1 
return x 
else: raise StopIteration 
sinifim = Sayilarim() 
yinelemem = iter(sinifim) 
for x in yinelemem: 
print(x)







Generatorler
Generatorler bellekte yer kaplamaz bu yüzden eger 100 bin tane sayiyi bir listeye atacaksak listeye atmaktansa generatorleri kullanmak daha mantikli. ‘’ yield ’’ kullanicaz. Ama uçucudur urettikten sonra siradakini uretince diğer geride kalanlar uçar gider. Mesela range fonksiyonu da boyle bellekte saklanmıyor.
def karelerial():
    sonuc = []
    for i in range(1,6):
        sonuc.append(i*i)
    return sonuc
print(karelerial())

#Generator ile kullanarak yapalim
def karelerial():
    for i in range(1,6):
        yield i**2;

generator =karelerial()
iterator = iter(generator)
next(iterator)
next(iterator)
next(iterator)
next(iterator)
next(iterator)

#Carpim tablosu yapalim
def carpimtablosu():
    for i in range(1,11):
        for j in range(1,11):
            yield "{} x {} = {}".format(i,j,(i*j))
            
for i in carpimtablosu():
    print(i)











PYQT5 ile Ara Yuz Gelistirme

	
import sys
from PyQt5 import QtWidgets

def pencere():
    app = QtWidgets.QApplication(sys.argv)
    pencere = QtWidgets.QWidget()
    pencere.setWindowTitle("ders1")
    pencere.show()
    sys.exit(app.exec_())

pencere()
ile pencere oluşturduk. 






import sys

from PyQt5 import QtWidgets
from PyQt5.uic.properties import QtGui


def pencere():
    app = QtWidgets.QApplication(sys.argv)
    pencere = QtWidgets.QWidget()
    pencere.setWindowTitle("ders1")
    etiket1 =QtWidgets.QLabel(pencere)
    etiket2 =QtWidgets.QLabelQ(pencere)

    etiket2.setPixmap(QtGui.QPixmap("resmin buradaki dosya uzantisi"))

    etiket1.setText("dsada") #ile kutunu icine deger yazariz.
    etiket1.move(150,30)# yazinin nerede olacagina karar verdik.
    etiket2.move(200,50)#resmin neredeolacagina karar verdik.
    
    pencere.show()
    sys.exit(app.exec_())

pencere()
 




Artik sadece fotograf koyuyorum kod solda cikti sagda
 












                      Pythton ile yuz tanima uygulamasi
1-https://github.com/opencv/opencv/tree/4.x/data/haarcascades sitesine git ve haarcascade.frontface.default.xml indir.
2- raw a basip dosyayi indirdikten sonra sayfayi farkli kaydet diyip masaustune indir
https://www.google.com/search?q=python+ile+y%C3%BCz+tan%C4%B1ma+uygulamas%C4%B1&rlz=1C1FHFK_trTR994TR994&sxsrf=ALiCzsbZFAL-NiU1XPGSPSPyJug1RF-8Pg:1668495926580&source=lnms&tbm=vid&sa=X&ved=2ahUKEwiX-IzYz6_7AhVvQ_EDHbjRA60Q_AUoAXoECAIQAw&biw=1280&bih=569&dpr=1.5#fpstate=ive&vld=cid:e0bb5234,vid:KCxF21anY1U buradan izle

                                     Django Nedir?
•	Pyhton programlama dilinin web kisminda kullanilan frameworktur.
•	Djangonun temel amaci karmasik olan web uygulamalarinin kullanimi kolaylastirmaktir.
•	Instagram,Mozilla,Pinterest.. Dijango kullanan web siteleri.
•	SQL sorgusu kullanilmiyor,objeler ile gerceklestiririz.
•	Model View Template  kullanilir.
•	Model  Dijango icindeki tablolar bulunur.
•	View  Response buradan doner yani ilgili url den ilgili response doner.
•	Template  Html kodlarimiz burada bulunur.
•	Database olarak default sqlite kullanir ORM oldugundan dolayi database kullanmaz. 
