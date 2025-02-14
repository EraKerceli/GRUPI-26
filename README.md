Programi i Dyqanit të Luleve

Ky program në C++ simulon një dyqan lulesh ku klientët mund të shikojnë llojet e luleve, të krijojnë buqetën e tyre, të zgjedhin nga ofertat speciale dhe të llogarisin çmimin përfundimtar bazuar në zgjedhjet e tyre. Programi përfshin gjithashtu oferta speciale për Shën Valentinin, zbritje për klientët e rinj dhe transport falas për porosi mbi 20 EUR.

Veçoritë
Llojet e Luleve: Shfaq një listë të luleve në dispozicion me çmimet përkatëse.

Krijimi i Buqetës: Lejon përdoruesit të zgjedhin lule dhe të krijojnë buqetën e tyre, me mundësinë e një zbritjeje prej 10% për klientët e rinj.

Oferta Speciale:
Oferta e Shën Valentinit: Bli një buqetë dhe merr një kartolinë dhe byzylyk falas.
Oferta 2+2: Bli një trëndafil dhe një tulipan dhe merr dy lule shtesë falas.

Transport Falas: Transport falas për porosi mbi 20 EUR.
Ndërveprimi me Përdoruesin: Programi udhëzon përdoruesit gjatë procesit të zgjedhjes duke siguruar një eksperiencë të lehtë dhe të këndshme.
Si Funksionon

Mesazhi i Mirëseardhjes: Kur programi nis, përdoruesit përshëndeten dhe shfaqen llojet e luleve në dispozicion me çmimet përkatëse.

Krijimi i Buqetës: Përdoruesit mund të zgjedhin lule për të shtuar në buqetë. Ata mund të specifikojnë sasinë e çdo lloji luleje që dëshirojnë.

Zbritje për Klientët e Rinj: Nëse përdoruesi është klient për herë të parë, ai merr një zbritje prej 10% në buqetën e tij.

Oferta Speciale:
Oferta e Shën Valentinit: Përdoruesi mund të zgjedhë midis dy buqetave të përgatitura paraprakisht dhe të marrë kartolinë dhe byzylyk falas.
Oferta 2+2: Nëse përdoruesi blen një trëndafil dhe një tulipan, ai mund të zgjedhë dy lule të tjera falas.

Llogaritja e Çmimit: Programi llogarit çmimin total bazuar në zgjedhjet e përdoruesit dhe aplikon çdo zbritje të vlefshme.
Transport Falas: Nëse çmimi total kalon 20 EUR, përfshihet transporti falas.
Struktura e Kodit
miresevini() – Përshëndet përdoruesin dhe e mirëpret në dyqan.

paraqitLule() – Shfaq listën e llojeve të luleve dhe çmimet e tyre.

formoBuqete() – Lejon përdoruesin të krijojë një buqetë sipas dëshirës.

ofertaShenValentin() – Shfaq ofertën speciale për Shën Valentinin.

zgjedhLuleFalas() – Lejon përdoruesin të zgjedhë lule falas si pjesë e ofertës 2+2.

oferta2plus2() – Menaxhon ofertën 2+2, duke lejuar përdoruesin të zgjedhë lule falas kur blen artikuj të caktuar.

main() – Funksioni kryesor që kontrollon rrjedhën e programit dhe udhëzon përdoruesin përmes të gjitha opsioneve.


bash
Copy
g++ -o flower_shop flower_shop.cpp
./flower_shop
Sample Output
sql
Copy
Miresevini ne dyqanin tone te luleve!

Llojet e luleve dhe cmimet per cope:
1. Trendafil - 3 EUR
2. Tulipan - 2 EUR
3. Orkide - 5 EUR
4. Zambak - 4 EUR

A jeni klient per here te pare? (po/jo): po
Si klient per here te pare, mund te formoni nje buqete dhe fitoni 10% zbritje!
Zgjidhni lule per te formuar buqeten tuaj. Kur te perfundoni, shtypni 0.
...

Cmimi total: 15 EUR
Transporti nuk eshte falas per blerje nen 20 EUR.
Faleminderit qe zgjodhet dyqanin tone te luleve!
License
This project is open-source and available under the MIT License.



