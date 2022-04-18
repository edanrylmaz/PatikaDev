# Örnek Dizi 1
**[22,27,16,2,18,6]** şeklinde verilen diziye Insertion Sort Algoritması uygulayacağız.
## Aşamalar
* Diziyi küçükten büyüğe doğru sıralamak istediğimizi düşünürsek algoritmaya göre ilk olarak dizinin ikinci elemanı ele alınır, bu eleman kendisinden bir önceki eleman ile kendi değerini karşılaştırır. Ele alınan eleman bir önceki elemandan küçükse önceki eleman sağa kaydırılır. Böylece ele aldığımız elemanı yerleştirebileceğimiz bir boşluk oluşur.
* Bu karşılaştırma işlemi işlem dizi sıralanana kadar devam eder.
* Bu örnekte ele alınan dizi değeri kalın ve italik olarak belirtilmiştir.

1. [22,<span style="color:red">***27***</span>,16,2,18,6] -> [22,27,16,2,18,6]
    * *Bu adımda 27 değeri ile 22 değeri karşılaştırılmış  27>22 olduğundan 27 değerinin yeri doğrudur.*
2. [22,27,<span style="color:red">***16***</span>,2,18,6] -> [<span style="color:red">***16***</span>,22,27,2,18,6]
    * *Bu adımda 16<27 olduğundan 27 değeri sağa kaydırılır ve 16 oluşan boşluğa yerleştirilir. Daha sonra 16 22 ile karşılaştırılır. 16<22 olduğundan 22 değeri sağa kaydırılır ve 16 oluşan boşluğa yerleştirilir.*
3. [16,22,27,<span style="color:red">***2***</span>,18,6] ->
[<span style="color:red">***2***</span>,16,22,27,18,6]
    * *Bu adımda sırasıyla 2<27, 2<22, 2<16 olduğundan her eleman sırayla sağa kaydırılır ve 2 oluşan boşluğa yerleşir.*
4. [2,16,22,27,<span style="color:red">***18***</span>,6] ->
[2,16,<span style="color:red">***18***</span>,22,27,6]
    * *Bu adımda sırasıyla 18<27 ve 18<22 olduğundan 27 ve 22 değerleri sağa kaydırılır ve açılan boşluğa 18 yerleşir.*
5. [2,16,22,27,18,<span style="color:red">***6***</span>] -> [2,<span style="color:red">***6***</span>,16,22,27,18]
    * *Bu adımda sorasıyla 6<18, 6<27, 6<22, 6<16 olduğundan gerekli sağa kaydırmalar yapılır ve 6 açılan boşluğa yerleştirilmiş olur.*
## Karmaşıklık Analizi
### Worst Case Time Complexity 
* O(n<sup>2</sup>) 
### Average Case Time Complexity
* O(n<sup>2</sup>)
### Best Case Time Complexity
* O(n)
* 18 değerine sahip dizi indexi worst case' girer.
# Örnek Dizi 2
**[7,3,5,8,2,9,4,15,6]** dizisin ilk dört adımı aşağıda verilmiştir.

1. [7,<span style="color:red">**3**</span>,5,8,2,9,4,15,6] -> [<span style="color:red">**3**</span>,7,5,8,2,9,4,15,6]
2. <span style="color:red">**7**</span> ele alınır ancak 7>3 olduğundan yeri değişmez.
3. [3,7,<span style="color:red">**5**</span>,8,2,9,4,15,6] -> [3,<span style="color:red">**5**</span>,7,8,2,9,4,15,6]
4. <span style="color:red">**8**</span> ele alınır ancak 8>7 olduğundan yeri değişmez.
5. [3,5,7,8,<span style="color:red">**2**</span>,9,4,15,6] -> [<span style="color:red">**2**</span>,3,5,7,8,9,4,15,6]