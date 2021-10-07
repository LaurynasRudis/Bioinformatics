# Pirmas laboratorinis darbas

## Įvadas

Šiame laboratoriniame darbe analizuojame 8 skirtingas virusų DNR sekas. Sekos gautos FASTA formatu.

**Bakterijų virusai**:
  1. Lactococcus_phage
  2. KM389305.1 UNVERIFIED: Escherichia phage CBA6 clone
  3. NC_028697.1 Streptococcus phage A25
  4. KC821626.1 Cellulophaga phage phi39:1

**Žinduolių virusai**:
  1. coronavirus
  2. adenovirus
  3. U18337.1 Variola virus Congo-1965
  4. herpesvirus
### 1. Koduojančių sekų radimas

Koduojančios sekos rastos iš fasta failuose nurodytų tiesioginių DNR sekų. Iš tiesioginės sekos buvo sudaryta jai koplementari atvirkštinė seka. Sekos tikrinimos po 3 simbolius iš eilės. Suradus start kodoną, toliau buvo ieškomas stop kodonas. Jei rastos sekos ilgis ne trumpesnis nei 100 kodonų, ta seka priskiriama baltymą koduojančioms sekoms. Sekų paieška atliekama 6 skaitymo rėmeliuose, 3 tiesioginėje sekoje (+1, +2 ,+3) ir 3 atvirkštinėje seko (-1, -2, -3).

### 2. Kodonų ir dikodonų dažnių radimas

Gautose koduojančiose sekose buvo skaičiuojamas kiekvieno galimo kodono ir dikodono kiekis. Gautas kiekis buvo padalinamas iš visų sekoje esančių kodonų ir dikodonų skaičiaus.  

### 3. Palyginimas tarp visų sekų

Palyginimui buvo panaudota atstumo formulė: <img src="https://render.githubusercontent.com/render/math?math=\sqrt(\sum(x_i%20-%20y_i)^2)"/>.
xi : pirmoje sekoje esančių kodonų/dikodonų dažnis, yi : antroje sekoje esančio kodono/dikodono dažnis. Gauti rezultatai išsaugomi PHYLIP formatu.

## Dažnių palyginimo rezultatai

### Kodonų 
#### Atstumų matrica
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
#### Medis

![codon_hierarchical](https://user-images.githubusercontent.com/47796168/136312966-2e1acea8-35bb-469c-8a20-9fdceefb01d4.png)

### Dikodonų
#### Atstumų matrica

```
8                                                                                                
Lactococcus_phage       0.0  0.021494  0.017372  0.027489  0.019422  0.022551  0.022053  0.027597
KM389305.1         0.021494       0.0  0.018826   0.03357  0.019215   0.01524  0.021612   0.01847
NC_028697.1        0.017372  0.018826       0.0  0.028053  0.016918  0.019398  0.021452  0.024258
KC821626.1         0.027489   0.03357  0.028053       0.0  0.028556  0.034092  0.028956  0.037906
coronavirus        0.019422  0.019215  0.016918  0.028556       0.0  0.018971  0.021282  0.024107
adenovirus         0.022551   0.01524  0.019398  0.034092  0.018971       0.0  0.022529  0.015396
U18337.1           0.022053  0.021612  0.021452  0.028956  0.021282  0.022529       0.0  0.026627
herpesvirus        0.027597   0.01847  0.024258  0.037906  0.024107  0.015396  0.026627       0.0
```

#### Medis

![dicodons_hierarchical](https://user-images.githubusercontent.com/47796168/136313169-3e099d7a-9e86-449c-b83d-52ee59a98c3f.png)

## Palyginimas

Atsižvelgiant į atstumų matricos meždius, galima pastebėti, jog kodonų ir dikodonų dažniai tarp žinduolių virusų ir bakterijų virusų dažniausiai skiriasi. Yra matomi variantai, kai žinduolio virusas (U18337.1 Variola virus Congo-1965) patenka į bakterijų virusų klasteri, o bakterijų virusas (KM389305.1 UNVERIFIED: Escherichia phage CBA6) patenka į žinduolių. Dikodonų ir kodonų dažnių medžiai yra pakankamai panašus. Abiejuose medžiuose labiausiai išsiskyrė NC_028697.1 Streptococcus phage A25 virusas, kuris sudarė savo atskirą šaką nuo likusių virusų.

### Dažniausiai pasitaikę kodonai ir dikodonai

![image](https://user-images.githubusercontent.com/47796168/136314654-ff7b5258-bb1e-43d3-bc55-c644518926df.png)



