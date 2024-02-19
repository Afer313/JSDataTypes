# **JavaScript-də Data növləri**

## **_JS-də 9 növ data mövcuddur:_**

- 1. String - Sətir
- 2. Number - Rəqəm
- 3. BigInt - Böyük rəqəm
- 4. Boolean - Bulean
- 5. Undefined - Dəyəri naməlum
- 6. Null - Dəyərsiz
- 7. Symbol - Simvol
- 8. Object - Obyekt
- 9. Array - Massiv (Array)
 
## __String__
 - Sətirlər JavaScript proqramlaşdırma dilində tək dırnaqlar `''`, qoşa dırnaqlar `""` və əks-dırnaqların arasına yazılır ` `` `. 
 - Sətir tipində olan məlumatlar üzərində biz riyazi əməliyyatlar apara bilmirik. Aparamağa calışdığımızda isə "+" operatoru ilə stringləri biri-o-birinin ardına düzürük və ya `TypeError` olan ` NaN ` cavabını alırıq. `NaN` (Not a number) abriviaturasıdır, əməliyyat aparmaq istədiyimiz dəyişqənlərin rəqəm olmadığını bildirir.
### Nümunə:
```javascript
let color = 'Yellow'; // Təkdırnaqlı yazılış qaydası
let name = "Kenny"; // Qoşadırnaqlı yazılış qaydası
let lastName = `Johnson`; //Əks-dırnaqlı yazılış qayası
```

## __Number__
- JavaScript-də rəqəm data növünə mövcudluqda daxildir: tam ədədlər, kəsirli ədədlər, eksponensial ədədlər.
- JavaScript-də ədədi dəyərlər toplama, çıxma, vurma və ədədlər arasında bölmə kimi əsas riyazi əməliyyatları yerinə yetirmək üçün istifadə olunur. JavaScript həm tam, həm də üzən nöqtəli ədədləri dəstəkləyir.

### Nümunə:

```javascript
let length = 16; // Tam ədəd
let weight = 7.5; // Kəsirli ədəd
let ekspo = 1.23e4; // Eksponensial ədəd
```
## __Bigint__
- JavaScript-də ixtiyari uzunluqdakı tam ədədləri təmsil etmək üçün istifadə edilən BigInt adlı başqa bir rəqəmsal məlumat növü var. Bu məlumat növü sizə nömrə növü üçün mövcud diapazondan kənar nömrələrlə işləməyə imkan verir.
- BigInts çox böyük tam ədədləri təmsil etmək və işləmək üçün bir yol təqdim edir və onlar, məsələn, riyazi hesablamalarda və ya kriptoqrafiyada böyük tam ədədlərlə işləyərkən faydalı ola bilər.

#### BigInt yaratmaq üçün rəqəmin sonuna `'n'` əlavə edə bilərsiniz:
### Nümunə:

```javascript
const bigIntValue = 1234567890123456789012345678901234567890n;
```
BigInt adi ədədlər kimi riyazi əməliyyatlarda istifadə edilə bilər:
### Misal:

```javascript
const bigIntA = 1234567890123456789012345678901234567890n;
const bigIntB = 9876543210987654321098765432109876543210n;

const sum = bigIntA + bigIntB;
const product = bigIntA * bigIntB;
```

## **Boolean**
- JavaScript-də Boolean məlumat növü iki mümkün Boolean dəyərini təmsil edir: doğru `(true)` və yanlış `(false)`.
-  Bu məlumat növü, Boolean nəticəsini qaytaran əməliyyatları yerinə yetirmək üçün və ya proqramın icrası axınına nəzarət etmək üçün istifadə olunur ki, kod şərtlər əsasında yerinə yetirilsin.

### Nümunə:
```JavaScript
const dogru = true;
const sehf = false;

if (dogru) {
  console.log("Bu şərt doğru olduğu üçün, icra olunacaq");
} else {
  console.log("Bu isə icra olunmayacaq.");
}
```

İstədiyiniz vaxtı [boolean](#javascript-booleans) -lar haqqında burdan daha əhtraflı məlumat ala bilərsiniz.

## __Undefined__
- "Müəyyən edilməmiş" JavaScript-də dəyişənin heç bir dəyəri olmadığını və ya müəyyən edilmədiyini göstərən primitiv dəyərlərdən biridir. 
- Dəyişən elan edildikdə, lakin işə salınmadıqda, ona avtomatik olaraq "müəyyən edilməmiş" dəyəri təyin edilir. 
- Bu, həmçinin heç bir qaytarma dəyəri olmadığı təqdirdə funksiyanın defolt olaraq qaytardığı dəyərdir.

### Nümunə:
```JavaScript
let ad;
console.log(ad); // Konsolumuza "undefined" yazısını çıxardacaq.
```
#### Və ya funsiya ilə:
```JavaScript
function numuneFunsiya() {
  // Bir 'return' yazmamışıq
}
const netice = numuneFunsiya();
console.log(netice); // Konsolumuza "undefined" yazısını çıxardacaq.
```
#### Mövcud olmayan obyektin xüsusiyyətinə daxil olmağa cəhd:
```JavaScript
const obj = { ad: "Məmmədəli" };
console.log(obj.soyad); // "undefined" qaytaracaq.
```
## __Null__
- "Null" JavaScript-də heç bir dəyər və ya boşluq göstərməyən xüsusi dəyər olan başqa bir primitiv məlumat növüdür.
-  Çox vaxt dəyişənin heç bir dəyəri olmadığını və ya dəyərin silindiyini açıq şəkildə göstərmək üçün istifadə olunur.

### Nümumə:
#### Bir dəyişənə açıq şəkildə "null" dəyərinin təyin edilməsi:
```JS
let name = null;
console.log(name); // Konsol-a "null" çıxaracaq.
```
#### "null" istifadə edərək dəyişəndən dəyərin silinməsi:
```JS
let name = "John";
name = null; // Dəyərin silinməsi
console.log(name); // Konsol-a "null" çıxaracaq.
```
#### "null" dəyərin mövcudluğunu yoxlamaq üçün istifadə edilə bilər:
```JS
let deyer = getSomeValue(); //Dəyər və ya 'null' qaytaran funksiya

if (deyer === null) {
  console.log("Dəyər mövcud deyil.");
} else {
  console.log("Dəyər mövcuddur: " + deyer);
}
```
## __Symbol__
- "Symbol" ECMAScript 6 (ES6) standartında təqdim edilmiş JavaScript-də unikal primitiv məlumat növüdür.
- Hər bir simvol unikal və dəyişməz identifikatoru təmsil edir.
- Onlar gizli və ya unikal obyekt xassələri və ya məlumatları saxlamaq üçün açarlar yaratmaq lazım olduqda faydalıdır.

### Nümunə:
Simvol `"new"` açar sözü olmadan `Symbol()` qlobal funksiyasından istifadə etməklə yaradılır. Bu funksiya tərəfindən yaradılan hər bir simvol unikaldır:

```JS
const simvol1 = Symbol();
const simvol2 = Symbol("Simvolun təsviri");
```
İkinci misalda siz simvolu təsvir etmək üçün istifadə olunacaq `Symbol()` funksiyasına sətir təqdim edə bilərsiniz (bu, onun unikallığına təsir göstərmir). Bu təsvir sazlama üçün faydalı ola bilər.

Simvollar, məsələn, obyektlərdə xassələrin açarları kimi istifadə edilə bilər:
```JS
const unikalAcar = Symbol("Unikal açar");
const obj = {};

obj[unikalAcar] = "Unikal açarla əldə edilə bilən dəyər";
console.log(obj[unikalAcar]); // "Unikal açarla əldə edilə bilən dəyər" konsol-a çıxacaq.
```
## __Object__
- JavaScript-dəki obyektlər, verilənləri `'açar-dəyər'` cütləri şəklində saxlamaq və təşkil etmək üçün istifadə olunur. 
- Onlar dilin əsas komponentlərindən biridir və hər yerdə istifadə olunur.
- Obyektdəki hər bir dəyər, bir açar tərəfindən saxlanılır və bu açar sətir və ya simvol ola bilər.
- Obyektdəki hər bir açar unikal olmalıdır.
### Bir obyekt yaratmaq və onunla işləmək nümunəsi:
```JS
// Obyektin yaradılması
const adam = {
  ad: "Hikmət",
  yas: 30,
  ixtisas: "proqramçı"
};

// Obyektin xassələrinə daxil olmaq
console.log(adam.ad); // Konsol-a "Hikmət" çıxaracaq.
console.log(adam.yas); // Konsol-a 30 çıxaracaq

// Obyektin xassələrində dəyişikliklər etmək.
adam.ixtisas = "dizayner";

// Yeni xassə əlavə etmək
adam.olke = "Turkiyə";

// Xassəni silmək
delete adam.yas;
```

### **Oybektlərin Datatype-ləri**
Obyektlərin daxilində bu tiplərdə məlumat saxlanıla bilər:

```md
1. Obyekt
2. Massiv
3. Date klassı
```

## __Array__
- JavaScript-də `"Array"` müxtəlif məlumat növlərində ola bilən sifarişli dəyərlər toplusudur.
-  Massivlər bir dəyişəndə ​​birdən çox dəyəri saxlamağa və bu məlumatları rahat manipulyasiya etməyə imkan verir.
#### Massiv yaratmaq və onun elementlərinə daxil olmaq kvadrat mötərizələrdən [] istifadə etməklə həyata keçirilir və hər bir element vergüllə ayrılır:
### Nümunə:
```JS
const myArr = [1, 2, 3, "Setir", true];
```
#### Massiv elementlərinə müraciət indekslər vasitəsilə olur (0-dan başlayaraq):
```JS
console.log(myArr[0]); // Konsola-a 1 çıxardacaq.
console.log(myArr[3]); // Konsol-a "Setir" çıxardacaq.
```
## VAÇİB:
#### Massivlər müxtəlif məlumat növlərinin elementlərini, o cümlədən ədədləri, sətirləri, booleanları, obyektləri və hətta digər massivləri ehtiva edə bilər.

#### Massivlərin onlarla əlaqəli müxtəlif üsulları və xassələri var ki, bu da onlara verilənlərin istifadəsini və manipulyasiyasını asanlaşdırır.
- Məsələn, elementləri əlavə edə, silə, massiv elementləri arasında təkrarlaya və daha çox digər əməliyyatlar edə bilərsiniz:

```JS
const reqemler = [1, 2, 3, 4, 5];

// Massivin sonuna element əlavə etmək.
числа.push(6);

// Massivin son elementin silinməsi.
числа.pop();

// Massivin elementləri üzərində itersiya aparılması.
числа.forEach(function(элемент) {
  console.log(элемент);
});

// Massivi uzunluğu
console.log(числа.length); // Konsol-a 5 qaytaracaq.
```
### Siz həmçinin `Array()` konstruktorundan istifadə edərək yeni massivlər yarada bilərsiniz:
```JS
const newArr = new Array(1, 2, 3);
```
- JavaScript-də massivlər məlumatların saxlanması, işlənməsi və təşkili üçün çox güclü vasitədir. Onlar dildə geniş istifadə olunur və onların necə işlədiyini anlamaq JavaScript tərtibatçıları üçün vacibdir.

<figure>
  <img
    src="https://www.bmrsolutions.co.uk/wp-content/uploads/Coding.jpg"
    alt="AnVIL Portal Image."
  />
</figure>


### __QEYD:__

```md
> JavaScript dəyişənlərinin istənilən dəyəri ola bilər.
```
