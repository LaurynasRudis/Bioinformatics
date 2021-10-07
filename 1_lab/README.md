# Pirmas laboratorinis darbas

## Įvadas

Šiame laboratoriniame darbe analizuojame 8 skirtingas virusų DNR sekas. Sekos gautos FASTA formatu.

### 1. Koduojančių sekų radimas

Koduojančios sekos rastos iš fasta failuose nurodytų tiesioginių DNR sekų. Iš tiesioginės sekos buvo sudaryta jai koplementari atvirkštinė seka. Sekos tikrinimos po 3 simbolius iš eilės. Suradus start kodoną, toliau buvo ieškomas stop kodonas. Jei rastos sekos ilgis ne trumpesnis nei 100 kodonų, ta seka priskiriama baltymą koduojančioms sekoms. Sekų paieška atliekama 6 skaitymo rėmeliuose, 3 tiesioginėje sekoje (+1, +2 ,+3) ir 3 atvirkštinėje seko (-1, -2, -3).

### 2. Kodonų ir dikodonų dažnių radimas

Gautose koduojančiose sekose buvo skaičiuojamas kiekvieno galimo kodono ir dikodono kiekis. Gautas kiekis buvo padalinamas iš visų sekoje esančių kodonų ir dikodonų skaičiaus.  

### 3. Palyginimas tarp visų sekų

Palyginimui buvo panaudota atstumo formulė: <img src="https://render.githubusercontent.com/render/math?math=\sqrt(\sum(x_i%20-%20y_i)^2)"/>.
xi : pirmoje sekoje esančių kodonų/dikodonų dažnis, yi : antroje sekoje esančio kodono/dikodono dažnis. Gauti rezultatai išsaugomi PHYLIP formatu.

## Dažnių palyginimo rezultatai

### Kodonų 

```
8                                                                                                
Lactococcus_phage       0.0  0.156577   0.08385  0.139824  0.109493    0.1908    0.1412  0.271439
KM389305.1         0.156577       0.0  0.125881  0.237139  0.148751  0.106226  0.181354   0.16439
NC_028697.1         0.08385  0.125881       0.0  0.158741  0.097265  0.151226  0.152538  0.235649
KC821626.1         0.139824  0.237139  0.158741       0.0  0.182315  0.267665  0.153014  0.333566
coronavirus        0.109493  0.148751  0.097265  0.182315       0.0  0.160688  0.159147  0.249387
adenovirus           0.1908  0.106226  0.151226  0.267665  0.160688       0.0  0.234198   0.11743
U18337.1             0.1412  0.181354  0.152538  0.153014  0.159147  0.234198       0.0  0.295588
herpesvirus        0.271439   0.16439  0.235649  0.333566  0.249387   0.11743  0.295588       0.0
```

