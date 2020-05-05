# CoinKing  ![alt text](rsz_7_1.png)
![alt text](4.png)

Kratka igrca, za mobilno napravo, v kateri s karakterjem premaguješ ovire, zbiraš žetone in z njimi trguješ v trgovini.

### Diagram primera uporabe

 ![alt text](1.png)
 
 Rezultat je viden v igri, med igranjom. Rezultat je tudi prenosljiv iz nivoja v nivo, ampak po trku z oviro se rezultat znova nastavi na 0 in se začne isti nivo od začetka. Prijava do določene mere ni potrebna saj se rezultat shranjuje na naši igralski platformi.

### E-R diagram 

  ![alt text](2.png)
  
  V naši končni verziji je število žetonov tudi enako končnemu rezultatu.

### Slike grafičnega vmesnika

 ![alt text](3.png)

Na menuju imamo 3 opcije. Po izbiri Play se nam začne igra. Če gremo na Shop nas preusmeri na vmesnik kjer lahko vidimo skine, ki bodo na voljo za nakup (work in progress). Na koncu pa še imamo Quit Game, ki nam zapre igro, ko hočemo prenehat igrat.

### Vodič za implementacijo kode, ki prenaša točke iz enega nivoja v drugega

Prvo moramo dodat datoteko iz našega projekta v vašega. Datoteko oziroma skripto, ki je potrebno dodat je ScoreCounter.cs (lahko tudi skupaj z ScoreCounter.cs.meta.).

![alt text](7.PNG)

Te datoteke dodate med vaše assests tako da se vam prikaže na tak način: 
![alt text](8.PNG)

