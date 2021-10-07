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

```python: viruses/results/codons_rate_distances.txt

