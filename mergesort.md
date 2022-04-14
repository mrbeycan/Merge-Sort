# Merge Sort

## Proje 2
### [16,21,11,8,12,22] -> Merge Sort

### Yukarıdaki dizinin sort türüne göre aşamalarını yazınız

- Liste çift sayıda elemandan oluşuyorsa ortadan , tek sayıda elemandan oluşuyorsa bir sadece tarafta bir eleman fazla olacak şekilde 2 parçaya ayırıyoruz.

- Ayırılan parçalar da kendi içlerinde tekrar iki parçailde bölüyoruz.
- Böldüğümüz ve her eleman tek başına kaldıktan sonra elemanları sıralı olacak şekilde tekrar liste helinde birleştiriyoruz.
- Fakat birleştirme işlemi yaparken sağ ve soldaki listeleirn ilk elemaları karşlıştırılır ve küçük olan listenin başına yazılır.
- Örneğin sağdaki listenin başındaki yani, listenin en küçük elemanı, soldaki listenin en küçük elemanından büyükse soldaki listenin en küçük elemanı yeni listenin başına yazılır. Sağdaki listenin en küçük elemanı soldaki listenin diğer elemanlarıyla kıyaslanır eğer soldaki listenin 2. elemanı büyükse bu sayı yeni listenin ikinci elemanı olarak yazılır.
- Eğer sağdaki listenin en küçük elemanı soldaki listenin ikinic elemanından da büyükse, yeni listeinin ikinici elemanı soldaki listenin ikinic elemanı olur.
  
### Aşağıda ki  görseli incelediğimizde olayı daha net kavrayacağız.

![MergeSort](https://upload.wikimedia.org/wikipedia/commons/e/e6/Merge_sort_algorithm_diagram.svg)

- Yukarıdaki merge sort örneginde ilk aşamlar olarak bize verilen liste sağ ve sol olmak üzere birer elemanlı listeler haline gelene kadar bölünmüş.
- Her elaman tek başına kalan kadar bölündükten sonra bu elemanlar sıralı hale gelecek şekilde birleştirilmeye başlanmış.

### [16,21,11,8,12,22]

- Dizi ilk aşamada      [16,21,11] ve [8,12,22] olarak bölüyoruz.
- İkinci aşamada      [16],[21,11] ve [8], [12,22] olarak bölüyoruz
- Üçüncü aşamada    [16],[21],[11] ve [8],[12],[22] olarak tek elemanlı kalana kadar böldük.
- Dörüdüncü aşamada  [11,16],[21]  ve [8,12],[22] olarak birleştiriyoruz.
- Beşinci aşamada     [11,16,21]   ve [8,12,22] olarak birleştiriyoruz.
- Altıncı aşamada         [8,11,12,16,21,22]  olarak birleştiriyoruz.
- Böylelikle listeyi insertion sort algoritmasından daha az sürede ve daha az enerji harcayarak sıralamış oluyoruz.

## Big-O gösterimini yazınız

- Merge Sort algoritması uygulanması için verilen dizi yada liste n/2 kere bölünmek için ve n/2 kere de birleştirilmek için işlem görüyor.
- 2^x = n ve x = logn oluyor. Bölme ve birleştirme  yaparak n işlem yapıyoruz ve bu durumda Big-O Notationumuz O(nlogn) olarak ortaya çıkıyor.
