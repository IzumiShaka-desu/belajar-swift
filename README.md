# belajar-swift
- Apa itu Swift
bahasa swift adalah bahasa pemrograman yang dikembangkan oleh apple inc. bahasa ini menjadi bahasa pengantar bagi mac developer,ios, watch os,dan platform apple lainnya. bahasa swift merupakan pengembangan dari bahasa Objective-c. selain itu Swift merupakan bahasa pemrograman yang modern, cepat, dan type-safe.
referensi pengenalan swift
https://medium.com/@rizal_hilman/swift-intro-apa-itu-bahasa-pemrograman-swift-b33ea3ce1a43
https://www.codepolitan.com/mengenal-swift-bahasa-pemrograman-untuk-teknologi-apple-589a92b4c2389
- Menggunakan REPL 
ha,rekayasa perangkat lunak atau rpl?. bukan-bukan, ini REPL atau Read Eval Print Loop adalah sebuah fitur untuk membaca, mengevaluasi, mencetak dan mengulang script dari suatu bahasa top-level. dalam bahasa swift penggunaan repl hanya perlu mengetikan perintah "swift" dan klik enter maka secara otomatis akan memasuki fitur repl milik swift.
contoh penggunaan repl
![Screenshot](screenshots/repl.png)
selain untuk mencoba kode program dengan bahasa swift kamu juga dapat secara otomatis menyarankan fungsi dan metode yang dapat digunakan dalam konteks tertentu. contoh penggunaannya
ketik => "Hi!".re 
lalu tekan tab
```
5> "Hi!".re
Available completions:
	remove(at: Index) -> Character
	removeAll() -> Void
	removeAll(keepingCapacity: Bool) -> Void
	removeSubrange(bounds: ClosedRange<Index>) -> Void
	removeSubrange(bounds: Range<Index>) -> Void
	replaceSubrange(bounds: ClosedRange<Index>, with: C) -> Void
	replaceSubrange(bounds: ClosedRange<Index>, with: String) -> Void
	replaceSubrange(bounds: Range<Index>, with: C) -> Void
	replaceSubrange(bounds: Range<Index>, with: String) -> Void
	reserveCapacity(n: Int) -> Void

```
- inisialisasi package executeable swift
untuk latihan pertama kita akan membuat sebuah folder bernama "Latihan" untuk package Latihan
```
mkdir Latihan
cd Latihan
```
lalu kita inisialisasi package executablenya
```
swift package init --type executable
```
secara default jika dijalankan dengan command 'swift run' maka script akan melakukan print "Hello, world!"

- variable dan const 
untuk melakukan deklarasi variable pada swift gunakanlah keyword var dan untuk deklarasi constant value gunakanlah let
contoh penggunaan
```swift
var myVariable = 42
myVariable = 50
let myConstant = 42
```
explicit type infersion, ketika mendeklarasikan variable kamu bisa menetapkan tipe data secara eksplisit sepert:
```swift
var nama: String = "akashaka"
var hariKe: Int = 2
```
nilai sebuah variable tidak pernah secara implisit di konvert menjadi tipe data yang sesuai, jadi kamu harus secara eksplisit mengubahnya, seperti:
```swift
let label = "The width is "
let width = 94
let widthLabel = label + String(width)
```
kamu bisa memuat nilai dari suatu variabel menjadi string dan memuatnya kedalam suatu string dengan cara seperti
```swift
let apples = 3
let oranges = 5
let appleSummary = "I have \(apples) apples."
let fruitSummary = "I have \(apples + oranges) pieces of fruit."
```

- array dan dictionaries
```swift
var testArray=["ayam goreng","rendang"]
var testArrayExplicit: String =["nasi goreng","es cendol"]
testArrayExplicit.append("ayam bakar")
var testDict=["nama":"akashaka","kelas":5]
var testDictExplicit: [String:String]=["nama":"nama","kelas":"5"]
var testDictExplicit["nama_lain":"shan"]
```

- Control Flow

Gunakan if dan switch untuk membuat kondisi, dan gunakan for-in, while, atau repeat-while untuk membuat perulangan. 
```swift
let individualScores = [75, 43, 103, 87, 12]
var teamScore = 0
for score in individualScores {
    if score > 50 {
        print("team score +3")
        teamScore += 3
    } else {
        print("team score +1")
        teamScore += 1
    }
}
print(teamScore)
```

dalam if statement, kondisi harus berupa boolean dimana kode seperti ```if score { ... }``` akan error, bukan sebuah perbandingan implisit terhadap nol.

kamu bisa menggunakan if dan let secara bersamaan pada variabel yang mungkin tidak memiliki nilai dimana berupa sebuah optional value. sebuah optional value dapat bernilai nil (dalam bahasa pemrograman lain null) yaitu sesuatu yang tidak memiliki nilai. untuk menandakan sebuah variabel adalah optional value kamu perlu menambahkan "?" setelah tipe data di deklarasikan.
```swift
var optionalString: String? = "Hello"
print(optionalString == nil)

var optionalName: String? = "Akashaka"
var greeting = "Hello!"
if let name = optionalName {
    greeting = "Hello, \(name)"
}
```
cara lain untuk memberikan nilai default pada sebuah optional value dengan menggunakan operator "??" seperti:
```swift
let nickname: String? = nil
let fullName: String = "John Appleseed"
let informalGreeting = "Hi \(nickname ?? fullName)"
```
switch pada swift mendukung banyak tipe data dan berbagai jenis operator perbandingan tidak terbatas pada integer dan test kesamaan nilai

```swift
let vegetable = "red pepper"
switch vegetable {
    case "celery":
        print("Add some raisins and make ants on a log.")
    case "cucumber", "watercress":
        print("That would make a good tea sandwich.")
    case let x where x.hasSuffix("pepper"):
        print("Is it a spicy \(x)?")
    default:
        print("Everything tastes good in soup.")
}
```
for in loop
```
 146> for i in 0...4{
 147.     print(i) 
 148. } 
0
1
2
3
4
 149> for i in 0..<4{
 150.     print(i) 
 151. } 
0
1
2
3

```
for in loop a dictionaries
```swift
let interestingNumbers = [
    "Prime": [2, 3, 5, 7, 11, 13],
    "Fibonacci": [1, 1, 2, 3, 5, 8],
    "Square": [1, 4, 9, 16, 25],
]
var largest = 0
for (_, numbers) in interestingNumbers {
    for number in numbers {
        if number > largest {
            largest = number
        }
    }
}
print(largest)
```
while and repeat while loop
```swift
var n = 2
while n < 100 {
    n *= 2
}
print(n)

var m = 2
repeat {
    m *= 2
} while m < 100
print(m)
```

