# CoinKing  ![alt text](rsz_7_1.png)
![alt text](4.png)

Kratka igrca, za mobilno napravo, v kateri s karakterjem premaguješ ovire, zbiraš žetone in z njimi trguješ v trgovini.

### Projekt

Projekt je možno pridobiti na tem linku: https://drive.google.com/file/d/1q4o-tjBjD4Si9ZGYNIpBOWtEmDtBXJ4h/view

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

Ko se vam prikaže skripta kot je prikazana na zgornji sliki potem morate samo še dodat tag na vašem objektu s katerem po trku želite, da se beležijo točke.
Se pravi prvo greste v SampleScenu na objekt katerega želite beležit (v našem primeru coin 1 in coin 2).

![alt text](9.PNG)

Ko izberemo objekt katerega želimo beležit z skripto mu nastavimo tag Coins.

![alt text](10.PNG)

Seveda pa lahko tudi tag spremenimo v kar koli drugega in v kodi tudi spremenimo pričakovani tag (v našem primeru je "Coins").
Gremo v ScoreCounter.cs in spremenimo if stavek kjer pričakuje tag Coins na isti tag kot smo prej si zamislili.

![alt text](11.PNG)

Kadar naredimo kot je zgoraj omenjeno nam mora na koncu igledati na tak način:

![alt text](12.PNG)

Če smo pravilno sledili navodilom lahko gremo v našo igro in testiramo. Testiramo na tak način, da poberemo prvi objekt in pogledamo zapis "Score:":

![alt text](13.PNG)

Za tem pa poberemo še en objekt pa bi se moralo inkrementirat za 1.

![alt text](14.PNG)

Po testiranju, če se nam na istem nivoju prenaša "Score" lahko gremo na drugi nivo (v našem primeru gremo v drevo). 

![alt text](15.PNG)

Na koncu pa še poberemo objekt na drugem nivoju in bi se zopet morala vrednost zvišat za 1 oziroma kolikor je vrednost nastavljena.

![alt text](16.PNG)

To shranjevanje nam omogoča vgrajena funkcija z imenom PlayerPrefs. PlayerPrefs je prav temu namenjeno, da se podatki shranjujejo med igralskimi sejami. Se pravi če enkrat zapremo igro in smo napredovali do določenega nivoja pa nočemo izgubiti naše žetone potem lahko samo igro zapremo in se ne sekiramo če so se nam žetoni ponovno resetirali na 0. Naša enostavna implementacija te funkcije v našo metodo pa skupaj naredi funkcijo, ki je enostavna, ponovno uporabna in delujoča.
