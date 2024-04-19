*Téma diplomovej práce je zameraná na analýzu obchodných dát z verejných obstarávaní, konkrétne kategorizáciu verejných obstarávaní na základe ich textového popisu do štandardizovaného klasifikačného systému Slovníka spoločného obstarávania (CPV). V práci sú zhrnuté teoretické poznatky týkajúce sa techniky spracovania prirodzeného jazyka (NLP), klasifikačných systémov CPV a ECLASS, architektúry Transformers a informácie o analýze obchodných dát i potenciálnych nedostatkoch v dátach verejných obstarávaní. Výkonnosť vybraných jazykových modelov BERT bola vyhodnotená na zvolených dátach verejných zákaziek vyhlásených v Českej republike, na základe mikro- a makro-metrík správnosti, presnosti, návratnosti a F1-skóre. Výsledky experimentov ukázali, ktoré verzie sú vhodnejšie pre klasifikáciu do hierarchickej schémy CPV.*

----------

- **preklad\_train\_final.csv:** Tréningová množina dát 35 446 záznamov verejných obstarávaní na klasifikáciu do klasifikačnej schémy CPV (1. a 2. úroveň)
- **preklad\_train\_final.csv:** Testovacia množina dát 15 192 záznamov verejných obstarávaní na klasifikáciu do klasifikačnej schémy CPV (1. a 2. úroveň)

----------

- **01_spracovanie-dat.ipynb:** Úvodné predspracovanie dát verejných obstarávaní z viacerých tabuliek
- **01_spracovanie-ICO.ipynb:** Spracovanie dát – identifikátory právnických osôb
- **01_spracovanie-CPV.ipynb:** Spracovanie dát – hierarchická schéma CPV, rozdelenie do tréningovej a testovacej množiny
- **02_anglicky-preklad.ipynb:** Preklad názvov a popisov verejných obstarávaní z českého do anglického jazyka
- **03_priprava-na-klasifikaciu.ipynb:** Informácie o kódoch CPV tréningovej a testovacej množiny dát
- **04_klasifikacia-existujuci-model.ipynb:** Klasifikácia hlavných záznamov verejných obstarávaní do 1. úrovne CPV pomocou modelu [MKaan/multilingual-cpv-sector-classifier](https://huggingface.co/MKaan/multilingual-cpv-sector-classifier)
- **05_klasifikacia-vyladeny-model.ipynb:** Ladenie modelov BERT ([google-bert/bert-base-multilingual-cased](https://huggingface.co/google-bert/bert-base-multilingual-cased), [Twitter/twhin-bert-base](https://huggingface.co/Twitter/twhin-bert-base) a [UWB-AIR/Czert-B-base-cased](https://huggingface.co/UWB-AIR/Czert-B-base-cased)) na klasifikáciu textu verejných obstarávaní do 2. úrovne CPV (ukážka, je potrebné určiť model BERT, počet epoch a pod.)