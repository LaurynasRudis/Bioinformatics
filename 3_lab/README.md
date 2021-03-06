# Trečias laboratorins darbas
## Naujos kartos sekoskaitos (NGS) duomenų analizė

<b>1. Apibūdinkite FASTQ formatą.</b>

 FASTQ – standartizuotas FASTA failo formatas, kuris dažniau naudojamas trumpoms sekoms aprašyti. Formato pradžioje pateikiama sekos, užkoduota ASCII formatu, skirta apibūdinti pateiktos sekos kokybei (tikslumą).
 
<b>2. Kurią mėnesio dieną Jūs gimėte? Prie dienos pridėkite 33. Koks ASCII simbolis atitinka šį skaičių?</b>

 11 + 33 = 44
 ASCII simbolis būtų , (kablelis).
 
<b>3. Kodėl pirmi 32 ASCII kodai negali būti naudojami sekos kokybei koduoti?</b> 
 
 Tai yra simboliai, skirti apibūdinti tam tikrą funkcinę klaviatūros mygtukų įvestį, nei kažkokį konkretų simbolį.
 
<b>4. Parašykite skriptą, kuris:</b> 
    
   <b>a) Nustatytu koks kokybės kodavimas yra naudojamas pateiktame faile. Parašykite, kokią koduotę nustatėte ir kuo remiantis?</b> 

   <b>Failo kokybės kodavimas</b>: Sanger Phred+33.  
   Nustatytas naudojant „bioinfokit“ bilbioteką. Pasinaudojus „analys.format.fq_qual_var(file)“ funkciją, kuri gražina failo kokybės kodavimo formatą.

   Koduotę galima atpažinti pagal naudojamus ASCII simbolius.
   Galimos koduotės:
   Sanger Phred+33, tipiškai naudoja 33-72 ASCII simbolius
   Solexa Solexa+64, tipiškai naudoja 59-104 ASCII simbolius
   Illumina 1.3+ Phred+64, tipiškai naudoja 64-104 ASCII simbolius
   Illumina 1.5+ Phred+64, tipiškai naudoja 57-105 ASCII simbolius
   Illumina 1.8+ Phred+33 , tipiškai naudoja 33-74 ASCII simbolius

   <b>b) Analizuotų C/G nukleotidų pasiskirstymą read’uose. Pateikite grafiką, kurio y ašyje būtų read’ų skaičius, x ašyje - C/G nukletidų dalis read’o sekoje (100 proc. reikštų, kad visi simboliai read’o sekoje yra G ir C). Parašykite, koks „stambių“ pikų skaičius yra gautame grafike.</b> 

   ### G/C nukleotidų dažnis read'uose
   ![image](https://github.com/LaurynasRudis/Bioinformatics/blob/main/3_lab/gc_count_graph.jpg?raw=true)

   Gauti 3 stambus pikai.

   <b>c) Paimtų po 5 kiekvieno piko viršūnės sekų ir atliktų blast’o paieškas. Naudokite nr/nt duombazę, paiešką apribokite taip, kad ieškotų atitikmenų tik bakterinės sekose (organizmas “bacteria”). Analizei naudokite tik patį pirmą atitikmenį. Pateikite lentelę, kurioje būtų read’o id ir rasto mikroorganizmo rūšis.</b> 

   Programa randa kiekvieno piko 5 sekas ir buvo atliekama online BLAST paieška. Žemiau yra pateikta lentelė su sekų ID ir pirmas paieškos rezultatas.

   ![image](https://user-images.githubusercontent.com/47796168/144335749-14a3c632-d57e-49de-b65a-2d8df6a763fc.png)



<b>5. Kokių rūšių buvo mėginyje?</b> 

Mėginyje buvo:

- Staphylococcus aureus (auksinis stafilokokas) - Gram teigiamos apvalios bakterijos, dažnai randama ant žmogaus odo ir viršutiniuose kvepavimo takuose. Gali sukelti odos bei kvepavimo takų ligas.
- Escherichia coli - Gram neigiamos, lazdelės formso bakterijos. Randamos šiltakraujų organizų žarnynuose. Gali sukelti žarnyno ligas.
- Thermus thermophilus - Gram neigiamos bakterijos, dažnai naudojamos biotechnologiniams tikslams. Bakterija itin termofiliška. Randama karštose versmėse.
