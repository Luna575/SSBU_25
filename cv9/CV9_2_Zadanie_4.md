## Zadanie 4 (5b)

V tomto zadaní budete pracovať s nástrojom MetaboAnalyst a datasetom: **NMR spectral bins**
    
`Binned 1H NMR spectra of 50 urine samples using 0.04 ppm constant width (Psihogios NG, et al.) Group 1- control; group 2 - severe kidney disease.`
    
Tento dataset je dostupný v sekcii 'Try our test data' v nástroji pre Jednofaktorovú štatistickú analýzu. 

Dataset pochádza z NMR-metabolomickej štúdie: Hodnotenie závažnosti tubulointersticiálnych lézií u pacientov s glomerulonefritídou. Začiatok tubulointersticiálnych lézií je charakterizovaný zníženým vylučovaním citrátu, hipurátu, glycínu a kreatinínu, zatiaľ čo po ďalšom zhoršení nasleduje glykozúria, selektívna aminoacidúria, úplné vyčerpanie citrátu a hipurátu a postupné zvyšovanie vylučovania laktátu, acetátu a trimetylamín-N-oxidu. Metabonomická analýza moču založená na NMR by mohla prispieť k včasnému hodnoteniu závažnosti poškodenia obličiek a prípadne k monitorovaniu ich funkcie. [1]


Načítajte množinu údajov v nástroji MetaboAnalyst. Pri filtrovaní údajov (Data filter) môžete použiť predvolené nastavenia.

### Úloha 1 (1b)

Normalizujte distribúciu datasetu (pre premenné aj vzorku).
(Vyberte akúkoľvek kombináciu operácií, ktorá je podľa Vás najlepšia).

**Ktoré operácie ste pri normalizácii použili?**

                    Sample normalization: # TODO = Normalization by Sum
                    Data Transformation:  # TODO = Square root transformation
                    Data Scaling:         # TODO = Auto scaling
### Úloha 2 (4b)

Použite ľubovoľné štatistické metódy na analýzu datasetu (napr. t-test, correlations, PCA, PLS-DA, Dendrogram, Heatmap, K-means, RandomForest, ..) 

**Uveďte aspoň 4 skutočnosti (z 4 rôznych metód), ktoré ste zistili analýzou datasetu:**

(Napr. Pri použití pearsonovho korelačného koeficientu je najvyššia pozitívna korelácia medzi premennými x a y, a koeficient korelácie je 0.992.)

                    1: # TODO = PCA - výsledkom sem dostali dva zhluky, na ktorých bolo vydieť že čo sa týka zdravých pacientov, tak ich dobre identifikovalo,
                    ale pokial by sme chceli identifikovať chorého pacienta tak to už by sa nedalo lebo zdravý sa prelínajú s chorými za to chorý sa nenachádzali 
                    v zhluku zdravých
                    2: # TODO = PLSDA - lepšie oddelila dáta na zhluky, aj keď vyzerá že medzi dátami môžu byť menšie výstreli:
                    C002 a C020 pri zdravých a P080 pri chorých, ale aj na priek tomu je jasne vidieť kde kto patrí
                    3: # TODO = Wilcoxon rank-sum test - hovorí že pri P-value = 0,01 je vea significantných hodnôt, ktorými vieme odlíšiť zdravého pacienta 
                    od nakazeného celkovo ich je 99 a najviac significantné vyzerajú byť Bin.2.70 a Bin.2.54
                    4: # TODO = Random forest = vyšiel tak že bez chybne sa vedel identifikovať zdravý pacient, no pri identifikovaní chorého už dochádzalo k menšej chybe (0,16)
                    medzi najpodstatnejšie hodnoty patril Bin.0.70 a potom sa zachovali tie dve z Wilcoxon rank-sum testu a outlineri z pacientov boli: P002,P037,P080,P113 a P099
                    

Vygenerujte report z vykonanej analýzy a celý výsledný zip file odovzdajte ako prílohu k riešeniu zadania.

----

#### Referencie

[1] Psihogios, N. G., Kalaitzidis, R. G., Dimou, S., Seferiadis, K. I., Siamopoulos, K. C., & Bairaktari, E. T. (2007). Evaluation of tubulointerstitial lesions’ severity in patients with glomerulonephritides: an NMR-based metabonomic study. Journal of Proteome Research, 6(9), 3760–3770. https://doi.org/10.1021/PR070172W
