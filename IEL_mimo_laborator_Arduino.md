# IEL v domácích podmínkách: Arduino a potřebné komponenty a alternativy

Článek je určen primárně pro ty, které IEL baví a chtějí experimentovat i mimo laboratoře - nebo naopak pro ty, kterým IEL moc nejde a chtěli by si vše procvičit předem nebo v klidu domova. 

Nejjednodušší je pořídit si nějaký starter kit, který obsahuje většinu věcí, které jsou potřeba. Starter kity se ale většinou zaměřují na programovatelnou elektroniku (což je mimochodem super oblast, vřele doporučuji ji alespoň prozkoumat), proto k nim je třeba dokoupit pár dalších komponent - a mnoho dalších vám bude v rámci IELu přebývat (ale znovu říkám, alespoň je vyzkoušejte! :)). V první části najdete odkazy na - dle mého názoru - dobré starter kity, ve druhé potom seznam komponent, kdybyste si ctěli složit "bare minimum IEL kit". Předem se omlouvám, pokud na nějakou součástku zapomenu, klidně udělejte PR s doplněním. Poslední kapitola bude takový krátký komentář k Arduinu, hlavně pro ty, kteří by měli o elektrotechniku, embedded a programovatelnou elektorniku zájem i nad (nebo spíš úplně mimo) rámec IELu. 

## Starter kity:

Kvalitní (a smysluplně sestavené) kity má https://www.laskakit.cz/ :

* Vyloženě elektro kit (bez Arduina atp): https://www.laskakit.cz/laskkit-midi-elektro-starter-kit/
	* Pro potřeby IELu bych asi doporučoval ten - na druhou stranu, oproti Arduinu má mnohem menší možnosti
	* Navíc k němu budete muset dokoupit obvod s hradly NAND a operační zesilovač (detaily v sekci o jednotlivých součástkách) 
	* Zdroj 5V napětí je realizovaný pomocí USB modulu
  
* Arduino MIDI starter kit: https://www.laskakit.cz/laskkit-arduino-midi-starter-kit/
	*  Ten obsahuje hromadu věcí , které v IELu nepoužíváme, ale lze z nich sestavit hromadu věcí okolo Arduina - LEDku, spínanou povelem z PC, ovládanou dálkovým ovladačem atp. - a to jsou všechno pouze naprosté základy, které lze s Arduinem udělat. K Arduinu lze připojit prakticky nekonečnou plejádu senzorů (senzory světla, IMU, senzory rozličných plynů...) a data z nich lze různě využívat.
	* Kromě jiného budete muset opět dokoupit obvod s hradly NAND  a operační zesilovač (detaily v sekci o jednotlivých součástkách) 
	* Zdroj 5V napětí bude zajišťovat samotné Arduino


## Další součástky a přístroje, která ve starter kitu nenajdete

### Multimetr

Už od první laboratoře pracujeme s multimetrem, zařízením, které umí měřit napětí, proud a odpor (a nejen to, ale v IELu nám to stačí). Stačí i poměrně levný, zhruba okolo 300-500:
* https://www.laskakit.cz/aneng-dm850-digitalni-multimetr/
* https://www.gme.cz/digitalni-multimetr-proskit-mt-1210

### Generátor signálů

V labinách pracujeme i s generátory signálů. Ten si v praxi musíte spájet sami, případně si ho naprogramovat sami pomocí Arduina (pro square waves). 
HELP WANTED: Kdo má zájem a čas, může udělat sketch pro Arduino, který by generoval obdélníkový signál o různé frekvenci. Sinus z Arduina bohužel bez dalších komponent nedostanete.
* Skládačku mají třeba v GME: https://www.gme.cz/stavebnice-generatoru-funkci-50hz-5khz
	Můžeme se bavit o pomoci se spájením, ale záleží na vašem počtu a momentálním časovém vytížení - možná vám to spájím hned, možná za měsíc, bohužel nemohu nic garantovat. 

### Osciloskop

Poslední součástí výbavy je osciloskop. Ten bohužel stojí od vyšších jednotek tisíc korun výše, takže si ho asi jen tak nepořídíte. Alternativou ovšem může být osciloskop DSO138, který pro základní zobrazení signálů bohatě stačí. Práce s ním není tak komfortní, ale dá se sehnat už za pár stokorun na Aliexpressu, případně do tisícovky v ČR. Dávejte si jen pozor, ať si objednáváte sestavený modul (presoldered/soldered module), tento osciloskop se prodává i ve formě stavebnice. 
* DSO138, hotová verze: https://www.laskakit.cz/digitalni-osciloskop-ds0138-200khz--spajena-verze/


## Pořízení jednotlivých komponent

Úplně odlišnou možností je pořídit si všechny součástky samostatně. Nebudu tu vypisovat konkrétní typy a odkazy na jejich pořízení, ale jen obecně popíšu, co byste si měli pořídit:

* Nepájivé pole: ideálně 400pinové, které plus minus odpovídá tomu, co používáme v labinách. Menší už nebývá tak hezky popsané, ale i jinak funguje stejně. 
* Rezistory: nejlepší je sada s různými hodnotami, nejvíce budete využívat ty v rozpětí stovek až stovek tisíc ohmů
* Potenciometr: standardní součástka (vypadá o dost ošklivěji než ty ve škole, ale funguje obdobně). Doporučuji dva-tři: s rozsahem 1k ohm a 10k ohm (případně i 100k ohm). Všechny lineární. 
* Kondenzátory: Minimum jsou nějaké v jednotkách uF a poté ve stovkách uF. Dají se pořídit keramické nebo elektrolytické. Elektrolytické se musí zapojit správně (minus na minus), jinak pro naše základy je to jedno. Detailní rozbor, jak se jednotlivé typy liší, najdete například zde: https://www.youtube.com/watch?v=2v8zBj7_sxg
* Propojoací vodiče: často se označují jako "dupont" a na rozdíl od těch v labinách mají hranaté koncovky. Existují v provedení M-M, F-M a F-F, M přitom znamená "samečka" (drátek), F "samičku" (objímku). Pro propojování jednotlivých řádků nepájivého pole se používají M-M kabely.
	Například: https://www.gme.cz/dupont-precizni-propojovaci-vodice-vidlice-vidlice-65-kusu pro M-M a https://www.gme.cz/propojovaci-vodice-vidlice-zasuvka-40-kusu pro F-M variantu
* IO s hradly NAND, například https://www.gme.cz/74hct00-dip14-texas-instruments Nemusí se jednat konkrétně o toto hradlo, ale v jeho názvu by se měl vskytovat řetězec "74HC00", možná proložený nějakým dalším písmenem, např. SN74HCT00N, SN74HC00N a podobně. 
    Zde upozorním, že budete muset zabrousit do datasheetu, abyste zjistili, na kterém pinu je která "funkce" čipu, neboli pinout. Datasheet dané součástky najdete jednoduše: do Googlu zadáte <název součástky> datasheet, kde <název součástky> budete mít na pouzdře. 
* Operační zesilovač, na labinách se používá MCP6021, který jsem ale v Česku nenašel. Alternativně lze (asi) použít LM741 https://www.gme.cz/lm741-dip8-texas-instruments . Ten má ale jiný pinout (vstupy a výstupy má na jiných nožičkách), tak se případně koukněte do datasheetu. 
* Svítivé diody (LEDky): asi není třeba představovat. Existují různé barvy a průměry, nějakou standardní LEDku mát třeba zde: https://www.gme.cz/led-5mm-red-2-50-hlmp-4700
* Normální diody: třeba 1N4007. Na laboratořích se používá jiná, ale to ničemu nevadí
* NPN tranzistor: např.  BC337-40 nebo 2N3904 (najdete třeba v GME po zadání uvedeného označení do vyhledávání)


## Pár poznámek
* Prakticky všechny věci (starter kity i jednotlivé součástky) lze koupit i na čínských online tržištích typu Aliexpress za zlomek ceny. Dodací lhůty jsou ovšem v řádu měsíců a záruka prakticky žádná. Nevýhody jsou ale často kompenzované právě cenou.
* Seznam není ani zdaleka vyčerpávající a stále je Work-in-Progress
* Značení součástek se liší podle data výroby, země původu, použití... Často ani nelze sehnat jednu konkrétní součástku a musíte pak shánět alespoň přibližnou alternativu (když mi vyjde, že mám použít 5kOhm rezistor - který se standardně nevyrábí - dám tam nejbližší hodnotu, co mám k dispozici, třeba 4.7kOhm). Jinak řečeno, každý elektrotechnik je tak trochu Jirka Babica :). 
* Pokud je někde napsané označení součástky (např BC337-40 nebo 7400), většinou ho nenajdete takhle "samo o sobě", ale bývá obalené spoustou dalších písmen (BC337-40BK, HC7400N), kde dodatečná písmena udávají např typ (TTL vs CMOS -  o tom se doslechnete i v IELu), teplotní a jinou odolnost, jakostní třídu a podobně. Často to také značí revizi obvodu. 
* V Brně sídlí obchod s elektornickými součástkami GME, najdete ho hned vedle Vaňkovky a zastávky šaliny 12 (Úzká).

## Arduino
TODO

TODOs
* Najít vhodný operační zesilovač se stejným pinoutem (přímá alternativa MCP6021)
* Dokončit sekci o Arduinu
* Doplnit seznam součástek ad hoc dle feedbacku