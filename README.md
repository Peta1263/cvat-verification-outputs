# Výstupy overenia funkčnosti modelov v prostredí CVAT

Tento repozitár obsahuje exportované výstupy z overenia funkčnosti modelov, ktoré boli integrované do prostredia CVAT v rámci bakalárskej práce.

Cieľom overenia nebolo hodnotenie presnosti modelov ani ich porovnanie s inými riešeniami. Overenie bolo zamerané na kontrolu, či modely dokážu prijať vstupnú fundus snímku, vykonať inferenciu a vrátiť výsledok vo forme použiteľnej v prostredí CVAT.

## Obsah repozitára

- `sam/` – výstupy z interaktívnej segmentácie pomocou modelu Segment Anything
- `lwnet/` – výstupy zo segmentácie ciev sietnice pomocou modelu LW-Net
- `dr_classifier/` – výstupy z klasifikácie diabetickej retinopatie pomocou ensemble klasifikátora

## Použité modely

### SAM

Model Segment Anything bol použitý na interaktívnu segmentáciu vybranej oblasti na fundus snímke. Ako segmentovaná oblasť bol zvolený optický disk. Výstupom bola editovateľná anotácia v prostredí CVAT.

### LW-Net

Model LW-Net bol použitý na segmentáciu ciev sietnice. Výstupom modelu bola maska ciev, ktorá sa v prostredí CVAT zobrazila ako masková anotácia.

### Ensemble klasifikátor

Ensemble klasifikátor bol použitý na klasifikáciu fundus snímok podľa stupňa diabetickej retinopatie. Výstupom bola trieda od `DR_0` po `DR_4`, ktorá sa v prostredí CVAT zobrazila ako tag priradený k celej snímke.

## Použité dáta

Na overenie modelu LW-Net boli použité fundus snímky z datasetu DRIVE.  
Na overenie ensemble klasifikátora a modelu SAM boli použité vybrané snímky z datasetu Diabetic Retinopathy 224x224 (2019 Data).
