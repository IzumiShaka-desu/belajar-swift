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
