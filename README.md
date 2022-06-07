# Veri_Yapilari_ve_Algoritmalar


# Insertion Sort

Insertion sort sıralı diziyi her adımda eleman eleman oluşturan bir sıralama algoritmasıdır.
Düzensiz dizi elemanlarını tek tek ele alarak her birini sıralanmış kısmındaki uygun yerine yerleştirme esasına dayanır.

Başta dizinin 2. elemanı seçilir ve öndeki elemanla karşılaştırma yapılır, eğer önündeki elemandan küçükse yer değiştirirler.
Bu işlem sonunda 3. eleman seçilir ve öndeki elemanlarla karşılaştırma yapılır, önündeki elemanlardan küçükse yer değiştirme işlemi yapılır.
Dizinin sonunda gelene kadar bu algoritma mantığı devam eder.

[22,27,16,2,18,6] Bu diziyi insertion sort algoritması ile sıralama işlemi yapacağız.

- Başlangıçta dizinin ikinci elemanı alınır ve en başa gidene kadar karşılaştırma işlemi yapılır.Burada 1 işlem gerçekleşir
        
[22, <span style ="color:red">**27**</span>,16,2,18,8]  --> 2.eleman olan 27 seçildi, öndeki elemansan büyük olduğu için yer değiştirme yapılmadı.

- Şimdi dizinin 3.elemanı seçilir ve önündeki elemanlarla karşılaştırma yapılır.

[22,27,<span style="color:red">**16**</span>,2,18,8] --> 3.eleman olan 16, 2. elemandan küçük yer değiştirme gerçekleşir.

[22,<span style="color:red">**16**</span>,27,2,18,8] --> 16 değeri 2.indexe geldi, önündeki değerden küçük olduğu için tekrar yer değiştirilir.

#### [<span style="color:red">**16**</span>,22,27,2,18,8] --> işlemler sonucu bu sıralama oluşur.

- Dizinin 4.elemanı olan **2** seçilir ve karşılaştırma işlemleri yapılır.

[16,22,27,<span style="color:red">**2**</span>,18,8] --> 2 değeri önündeki değerden küçüktür.

[16,22,<span style="color:red">**2**</span>,27,18,8] --> 2 değeri önündeki değerden küçüktür.

[16,<span style="color:red">**2**</span>,22,27,18,8] --> 2 değeri önündeki değerden düşüktür ve başa gelir.

#### [<span style="color:red">**2**</span>,16,22,27,18,8] --> işlemler sonucu bu sıralama oluşur.

- Dizinin 5. elemanı olan 18 seçilir ve karşılaştırma işlemi yapılır.

[2,16,22,27,<span style="color:red">**18**</span>,8] --> 18 değeri önündeki değerden küçüktür.

[2,16,22,<span style="color:red">**18**</span>,27,8] --> 18 değeri önündeki değerden küçüktür.

[2,16,<span style="color:red">**18**</span>,22,27,8] --> 18 değeri önündeki değerden büyüktür.

#### [2,16,<span style="color:red">**18**</span>,22,27,8] --> işlemler sonucunda bu sıralama oluşur.

-Son eleman olan 8 değeri seçilir ve karşılaştırma işlemleri yapılır.

[2,16,18,22,27,<span style="color:red">**8**</span>] --> 8 değeri önündeki değerden küçüktür.

[2,16,18,22,<span style="color:red">**8**</span>,27] --> 8 değeri önündeki değerden küçüktür.

[2,16,18,<span style="color:red">**8**</span>,22,27] --> 8 değeri önündeki değerden küçüktür.

[2,16,<span style="color:red">**8**</span>,18,22,27] --> 8 değeri önündeki değerden küçüktür.

[2,<span style="color:red">**8**</span>,16,18,22,27] --> 8 değeri önündeki değerden büyüktür.

#### [2,<span style="color:red">**8**</span>,16,18,22,27] --> işlemler sonucunda bu sıralama oluşur ve dizi Insertion Sort Algoritmasına göre sıralanmış olur.


### Big O

Big O gösterimi : (n-1)+(n-2)+(n+3)+...+1 = (n(n-1))/2 = n^2 sonucuna ulaşırız.
 ##### Sonuç : O(n^2)

### Time Complexity

Best Case : Dizinin sıralı olması. **n**

Worst Case : Dizinin tersten sıralı olması : **n^2**

Average Case : Dizinin normal dağılımı : **n^2**

#### Dizi sıralandıktan sonra 18 sayısı dizinin ortalarında olur.Bu sebeple <span style ="color:red">***Average Case***</span> kapsamına girer

-----

#### [7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımı

1. [7,<span style="color:red">**3**</span>,5,8,2,9,4,15,6] --> 2.eleman olan 3 seçilir ve karşılaştırma yapılır.
2. [3,7,<span style="color:red">**5**</span>,8,2,9,4,15,6] --> 3.eleman olan 5 seçilir ve karşılaştırma yapılır.
3. [3,5,7,<span style="color:red">**8**</span>,2,9,4,15,6] --> 4.eleman olan 8 seçilir ve karşılaştırma yapılır.
4. [3,5,7,8,<span style="color:red">**2**</span>,9,4,15,6] --> 5.eleman olan 2 seçilir ve karşılaştırma yapılır.

#### 4.adımın sonunda oluşan dizi [2,3,5,7,8,9,4,15,6] olur.



---
# Merge Sort

Bu algoritma diziyi ardışık olarak en küçük alt dizilere yarılar ve tek bir eleman kalana kadar bu işleme devam eder. 
Tek kalan elemanları birbirleri ile karşılaştırarak tekrar birleştiren algoritmadır.
 
                            [16,21,11,8,12,22] 

Bu diziyi merge sort algoritması ile sıralayacağız.

| İşlemler                                                                                                   | Elemanlar                             |
|------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Dizi elemanları yazılır.                                                                                   | [16,21,11,8,12,22]                    |
| Bu dizi yarılanır ve iki alt dizi oluşturulur.                                                             | [16,21,11]  ---- [8,12,22]            |
| Dizi tekrar yarılanır. Alt kümelerin eleman sayısı 3 olduğu için 2 ve 1 olarak ayrılırlar.                 | [16] --- [21,11] ---- [8] --- [12,22] |
| Tekrar bölünme işlemi yapılır ve her elemanın tek kalması sağlanır.                                        | [16] --- [21] -- [11] ---- [8] --- [12] -- [22] |
| Elemanlar tek kaldıktan sonra birleştirme işlemi başlar.(Tire sayısı az olanlar ilk sıraya göre birleşir.) | [16] --- [11,21] ---- [8] --- [12,22] |
| Sıralama ve birleştirme işlemi devam eder.                                                                 | [11,16,21] ---- [8,12,22] |
| Birleşme işlemi sonunda 2 alt dizi kaldı bunlar da kendi aralarında birleşerek sıralamayı tamamlarlar.     | [8,11,12,16,21,22] |

Böylelikle sıralama işlemi bitmiş olur.

Elemanların birleşme işlemi sırasında dizilerde en soldaki eleman en küçük elemandır, en sağdaki eleman ise en büyük elemandır.
Bunu bilir ve buna göre hangisi daha küçükse birleşen dizide en küçük eleman olarak yazılır, bu karşılaştırma işlemi alt dizilerde devam eder bir üst diziye sıralanmış şekilde gelirler.

## Big O Gösterimi 

- Diziyi parçalara ayırırken sürekli yarıladık yani 2'ye böldük. Bunun sonucunda

                                        2^x=n ==> logn
kere bölme işlemi yapmış oluruz.

- Bölünmüş diziyi birleştirirken dizinin uzunluğu olan n kadar birleştirme işlemi yapılır.
Bunun sonucunda algoritmanın maliyeti Big O Notasyonunda

                                        O(n.logn)

sonucuna ulaşılır.
Bizim dizimizde eleman sayısı 6 olduğu için sonuç
 
                                        6.log6 

olacaktır.

## BinarySearchTree

root 7

5, 7 den küçük olduğu için soluna gelir

1, 7 ve 5 den küçük olduğu için 5 in soluna gelir

8, 7 den büyük olduğu için 7 nin sağına gelir

3, 7 ve 5 den küçük fakat 1 den büyük olduğu için 1 in sağına gelir

6, 7 den küçük 5 den büyük olduğu için 5 in sağına gelir

0, 7,5 ve 1 den küçük olduğu için 1 in soluna gelir

9, 7 ve 8 den büyük olduğu için 8 in sağına gelir

4, 7,5 den küçük fakat 1 ve 3 den büyük olduğu için 3 ün sağına gelir

2, 7,5 den küçük 1 den büyük fakat 3 den küçük olduğu için 3 ün soluna gelir.

### https://app.patika.dev/emrevaljean

