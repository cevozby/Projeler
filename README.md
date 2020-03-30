# Sorting-Algorithm
Big O() nedir:
Basit bir şekilde matematiksel olarak anlatmaya çalışırsak f ve g fonksiyonları reel sayı olursa;

f(x) fonksiyonu c ve k sabit olmak üzere büyük O fonksiyonu O(g(x)) şeklinde tanımlanır.

•|f(x)| ≤ c|g(x)|+k

x > k olmalı.

Big O() nasıl hesaplanır:
O(1);
Büyüme sayısı 1'dir. Sadece tek seferlik çalışan herhangi bir döngü içermeyen yazılımlardır. (Örneğin if komutu.)
O(n);
n elemanlı bir döngü, n kere döndüğü için n kez işlem yapar. Başka döngülerin bulunmadığı durumdur.
O(n^c);
n eleman sayısı c ise iç içe döngü sayısıdır. İç içe iki döngüden oluşuyosa O(n^2) olur. Karıştırılmaması gereken husus eğer döngüler iç içe değilse n elemanlı bir döngü ve m elemanlı başka bir döngü varsa O(n+m) olur.
O(logn);
Eğer döngü içerisinde sürekli bölme veya çarpma işlemi yapılıyorsa log(n) karmaşıklığı oluşur.

SORTİNG

Seçerek Sıralama: Big O(n^2)
Her adımda dizideki en küçük sayıyı bulur ve sırasıyla dizinin başına atar. Adım adım gösterimi;
1)	Başlangıç olarak i=0 ayarla.
2)	Dizideki en küçük sayıyı bul
3)	Bu en küçük sayının yeri ile dizinin 0. elamanının yerini değiştir
4)	i’yi bir arttır ve 2. adıma git.

Hızlı Sıralama: Big O(n*log(n))
Dizide orta noktada bulunan bir sayıyı alır ve bütün sayıları bu değerden küçük veya büyük diye sınıflayarak sıralama yapar. Adım adım gösterimi;
1)	n elemanlı bir dizide ortadaki sayı bulunur yani n/2’inci eleman.(Eğer tek sayı ise (n-1)/2 olacak)
2)	1. adımdaki sayıya göre elemanlar küçük ve büyük diye sınıflandırılır. (Eğer en büyük/küçük sayı seçildiyse geriye kalan bütün sayılar küçük/büyük olacaktır.)
3)	Elimizde orta sayıdan küçük ve büyük değerlerin sınıfları olduğu için artık her 2 sınıf kendi arasında orta değer bulunarak sıralanacak. 

Birleştirme Sıralaması: Big O(n*log(n))
Diziyi ikişer elemanı kalana kadar sürekli ikiye böler. Sonra bu parçaları kendi içlerinde sıralayarak birleştirir. Sonucunda elde edilen dizi sıralı dizinin kendisidir. Adım adım gösterimi;
1)	Diziyi ikişer gruplar haline getirene kadar böl.
2)	Eleman sayısı 2 veya 1 ise dur.
3)	Her parçayı kendi içinde sırala
4)	Bölünmüş parçaları birleştir ve birleştirirken sıraya dikkat ederek birleştir.
5)	Her birleşen parçayı kendi içinde sırala.
6)	Bütün parçalar birleşince dur. 

Yığınlama Sıralaması: Big O(n)
Arka plan bir ağaç oluşturur ve bu ağacın en üstündeki sayıyı alarak sıralama işlemini yapar. En büyük sayı her zaman en üstte durur. En büyük sayıyı aldıktan sonra dizinin en başına atar. Yani dizi büyükten küçüğe doğru sıralanır.
Sayarak Sıralama:
Dizideki her sayıdan kaç tane olduğunu sayar ve bunu başka bir diziye atar. Sonra bu sayıların bulunduğu dizinin üzerinde bir işlemle sıralanmış olan diziyi elde eder.

Kabarcık Sırlaması: Big O(n^2)
Ardışık iki sayıyı karşılaştırır ve büyük veya küçük olması durumuna göre yer değiştirir. En büyük eleman en sağa gider ve bu işlem azalarak devam eder.  Adım adım gösterimi;
1)	İlk iki sayıyı al.
2)	İki sayıyı karşılaştır.
3)	Küçük olanı sol tarafa yaz ve diğerini hafızada tut.
4)	Dizinin sonuna geldiysen hafızadaki sayıyı yaz.
5)	Dizinin sonu değilse yeni bir sayı al.
6)	2. adıma geri git. 

Taban Sıralaması: Big O(basamak sayısı*n)
Sıralanacak olan değerler basamak basamak sıralanır.  1’ler basamağından başlayarak en büyük sayı kaç basamaklıysa ona göre sıralar. Her basamağı kendi içinde sıralar. Adım adım gösterimi;
1)	1’ler basamağını kendi içinde sırala.
2)	10’lar basamağını kendi içinde sırala.
3)	10^n’ler basamağını kendi içinde sırala. 

Sokma Sıralaması: Big O(n^2)
Dizinin 1. elemanından başlayarak sonunca elamanına kadar birer birer arttırıp grup oluşturur ve kendi aralarında sıralar. Adım adım gösterimi;
1)	Dizinin ilk elemanını alır ve karşılaştırma yapar. 
2)	Dizinin ikinci elamanını alır ve birinci eleman ile karşılaştırma yapar.
3)	Dizinin üçüncü elemanını alır, birinci ve ikinci elemanlar ile karşılaştırma yapar.
4)	Dizinin sonuncu elemanını alır ve dizinin geri kalan bütün elemanları ile karşılaştırma yapar. 

Sallayıcı Sıralaması: Big O(n^2)
Yapı olarak kabarcık sıralamasına benzer. Kabarcık sıralamasından tek farkı seçili olan elemanı hem sağındaki hem de solundaki eleman ile karşılaştırır. Bu nedenle çift yönlü kabarcık sıralaması da denilebilir.

Kabuk sıralama: Big O(n^2)
Sıralama işlemi için önce miktar belirtilir. Örneğin miktar sayımız “n” olsun. Sırasıyla her sayıyı “n” kadar sonraki sayı ile karşılaştırır.

Rastgele Sıralama: Big O(n*n!)
Diziyi sıralamak için rastgele bir dizilim üretir ve kontrol eder. Eğer dizi sıralı değil ise tekrar bir rastgele dizilim üretir. Sayılar sıralanıncaya kadar bu işlem devam eder. 

Serseri Sıralaması: Big O(nlog(3) / log(1.5)) = O(n2.8)
Diziyi sürekli 2/3 oranında parçalara bölerek kalan sayıları kendi aralarında sıralar. 

Tarak Sıralaması: Big O(n*log(n))
Kabarcık sıralamasının daha genel bir halidir. Kabacık sıralamasında hemen yanındaki ile karşılaştırırken tarak sıralamasında mesafe herhangi bir sayı olabilir.

Gnome Sıralaması:
İlk elemandan başlayarak dizideki diğer elemanlarla karşılaştırma yapar. Eğer büyükse yer değiştirirler. Aynı eleman bu sefer bir sonraki sırada eleman ile karşılaştırılır. Eğer sağındaki eleman kendisinden küçük ise küçük sayı sol tarafa geçer ve sola doğru sürekli karşılaştırma yapılır. Sonra değişen elemanımıza tekrar döner ve tekrardan karşılaştırma yapar. 
Permütasyon sıralaması: Big O(n*n!)
Dizinin uzunluğu “n” olsun. n! kadar ihtimal vardır ve bütün ihtimallere bakar. Sıralı olan haliyle karşılaşınca durur.

İplik Sıralaması:
İki tane data oluşturur ve elemanları ikisine ayırır. İki data arasındaki elemanları sırasıyla karşılaştırır ve küçük olan eleman ilk dataya geçer. 
