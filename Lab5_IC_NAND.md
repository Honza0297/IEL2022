Předchozí labiny byly zaměřené na relativní základy a zapojování z jednotlivých součástek. Všechny součástky, jednu po druhé, jsme zapojovali do nepájivého pole. Tentokrát už ale budeme pracovat s integrovaným obvodem (ang. Integrated Circuit, IC), kde už jednotlivé součástky neuvidíme a budeme se muset spoléhat na pinout a schéma. Mimochodem, kdo během posledních labin nevěděl, jak se měří napětí, jak fungují logická hradla, RC články nebo jak je propojená bastldeska (neboli nepájivé pole :), výrazně doporučuji se všechno doučit. V dalších labinách už na tyhle základy nebude čas. 

Níže opět přikládám seznam videí, která vám třeba pomohou:
* Co to je integrovaný obvod. Obecný úvod, který není pro labinu nutný, ale dá vám základní představu, co to ten integrovaný obvod (neboli "šváb") je: https://www.youtube.com/watch?v=drtUkvtxp6s 

*  Intro do logických bran. Tohle video využijí ti, kteří se neorientují v tom, jak jsou logické funkce vytvářené a zakreslované v elektrotechnice, případně si nebyli jistí Experimentem 3 předchozí labiny: https://www.youtube.com/watch?v=fw-N9P38mi4 
    
    ^Video obsahuje pouze NOT, AND, OR brány. My budeme pracovat navíc s NAND - představte si bránu AND, na jejíž výstup je ještě připojená brána NOT.

* Na labině se pracuje s IC, který v sobě ukrývá 4 dvouvstupé brány NAND. Tyto IC se standardně označují jako "typ 7400". V realitě je ale kolem čísel "7400" ještě hromada písmen, určujících konkrétní vlastnosti toho onoho čipu (o trochu podrobněji to rozebírám v https://github.com/Honza0297/IEL2022/blob/master/IEL_mimo_laborator_Arduino.md#p%C3%A1r-pozn%C3%A1mek). Od čipů 7400 je i (přímo či nepřímo) odvozených mnoho podobných čipů.  Pro zájemce doporučuji tohle video (ovšem k labině ho nepotřebujete): https://www.youtube.com/watch?v=Ki8mvWAVUsU

* Zde se vysvětluje, jak pracovat s jedním hradlem NAND: https://www.youtube.com/watch?v=nkQhaQmv7iE

Následně bude nutné zapojit bistabilní a astabilní obvody, vždy ze dvou hradel NAND.

* Začneme s bistabilním obvodem, neboli "RS NAND latch", jak se obvodu říká v angličtině: https://www.youtube.com/watch?v=-aQH0ybMd3U

    ^ o RS NAND latch se mluví až cca od 8. minuty, ale doporučuji si projít celé video. 

* Druhým obvodem, který si zkusíte zapojit, je astabilní klopný obvod (astabilní multivibrátor). Je poměrně těžké najít video, kde by se obvod jak ukazoval, tak hezky vysvětloval, proto sem dám několik videí a stránek, které dohromady vytváří celkový obraz:
    * https://www.youtube.com/watch?v=yuXeBstLm_w - ukázka toho, jak astabilní obvod "bliká". Zapojení je ovšem děsné a nepřehledné. 
    * https://www.youtube.com/watch?v=oQ5YzUCo8Pg - astabilní klopný obvod, ovšem z tranzistorů. My budeme místo tranzistorů používat NAND hradla, ale princip příliš rozdílný nebude. 
    * https://www.youtube.com/watch?v=cnVNj7jVGUg - astabilní multivibrátor s jednou LED (my budeme používat dvě) a pár dalšími změnami na čipu 4011, což je jen CMOS verze čipu 7400 (celá řada 74xx(x) je TTL, alespoň ty starší Teslácké čipy). V tomhle videu se ovšem vysvětluje vliv kapacity kondenzátoru na rychlost kmitání, takže doporučuji. K videu je i pěkný článek, kde se popisují detaily zapojení: http://www.learningaboutelectronics.com/Articles/Astable-multivibrator-with-a-4011-NAND-gate.php 

Pár poznámek závěrem
---
* Na IC se vyskytují takové "výkusy", které jsou vidět například na obrázku https://upload.wikimedia.org/wikipedia/commons/c/c6/TexasInstruments_7400_chip%2C_view_and_element_placement.jpg v levé části čipu. Tyto výkusy určují orientaci. 
* Bistabilní obvod je takový, který se ustálí v jednom ze dvou stavů. Astabilní se neustálí nikdy a monostabilní má jen jeden stav, na kterém se ustálí. 

Co byste měli umět:
---
* Jak fungují logická hradla AND, OR, NOR, NAND, XOR. Ne nutně uvnitř na úrovni tranzistorů, ale alespoň na úrovni vstupů a výstupů.
*  Co je to RS latch.
*  Proč astabilní klopný obvod bliká.
