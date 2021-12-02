# Trečias laboratorins darbas
## Naujos kartos sekoskaitos (NGS) duomenų analizė

1. Apibūdinkite FASTQ formatą. 
 FASTQ – standartizuotas FASTA failo formatas, kuris dažniau naudojamas trumpoms sekoms aprašyti. Formato pradžioje pateikiama sekos, užkoduota ASCII formatu, skirta apibūdinti pateiktos sekos kokybei (tikslumą).
2. Kurią mėnesio dieną Jūs gimėte? Prie dienos pridėkite 33. Koks ASCII simbolis atitinka šį skaičių? 
11 + 33 = 44
ASCII simbolis būtų , (kablelis).
3. Kodėl pirmi 32 ASCII kodai negali būti naudojami sekos kokybei koduoti? 
 Tai yra simboliai, skirti apibūdinti tam tikrą funkcinę klaviatūros mygtukų įvestį, nei kažkokį konkretų simbolį.
4. Parašykite skriptą, kuris: 
    a) Nustatytu koks kokybės kodavimas yra naudojamas pateiktame faile. Parašykite, kokią koduotę nustatėte ir kuo remiantis? 
        Failo kokybės kodavimas: Sanger Phred+33.  Nustatytas naudojant „bioinfokit“ bilbioteką. Pasinaudojus „analys.format.fq_qual_var(file)“ funkciją, kuri gražina failo kokybės kodavimo formatą.

    Koduotę galima atpažinti pagal naudojamus ASCII simbolius.
    Galimos koduotės:
    Sanger Phred+33, tipiškai naudoja 33-72 ASCII simbolius
    Solexa Solexa+64, tipiškai naudoja 59-104 ASCII simbolius
    Illumina 1.3+ Phred+64, tipiškai naudoja 64-104 ASCII simbolius
    Illumina 1.5+ Phred+64, tipiškai naudoja 57-105 ASCII simbolius
    Illumina 1.8+ Phred+33 , tipiškai naudoja 33-74 ASCII simbolius
    
    b) Analizuotų C/G nukleotidų pasiskirstymą read’uose. Pateikite grafiką, kurio y ašyje būtų read’ų skaičius, x ašyje - C/G nukletidų dalis read’o sekoje (100 proc. reikštų, kad visi simboliai read’o sekoje yra G ir C). Parašykite, koks „stambių“ pikų skaičius yra gautame grafike.

    ### G/C nukleotidų dažnis read'uose
        ![image](https://github.com/LaurynasRudis/Bioinformatics/blob/main/3_lab/gc_count_graph.jpg?raw=true)

    Gauti 3 stambus pikai.

    c) Paimtų po 5 kiekvieno piko viršūnės sekų ir atliktų blast’o paieškas. Naudokite nr/nt duombazę, paiešką apribokite taip, kad ieškotų atitikmenų tik bakterinės sekose (organizmas “bacteria”). Analizei naudokite tik patį pirmą atitikmenį. Pateikite lentelę, kurioje būtų read’o id ir rasto mikroorganizmo rūšis.

    Programa randa kiekvieno piko 5 sekas ir buvo atliekama online BLAST paieška. Žemiau yra pateikta lentelė su sekų ID ir pirmas paieškos rezultatas.



5. Kokių rūšių buvo mėginyje?

Mėginyje buvo:

- Staphylococcus aureus (auksinis stafilokokas) - Gram teigiamos apvalios bakterijos, dažnai randama ant žmogaus odo ir viršutiniuose kvepavimo takuose. Gali sukelti odos bei kvepavimo takų ligas.
- Escherichia coli - Gram neigiamos, lazdelės formso bakterijos. Randamos šiltakraujų organizų žarnynuose. Gali sukelti žarnyno ligas.
- Thermus thermophilus - Gram neigiamos bakterijos, dažnai naudojamos biotechnologiniams tikslams. Bakterija itin termofiliška. Randama karštose versmėse.
