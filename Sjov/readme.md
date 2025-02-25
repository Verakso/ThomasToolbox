# Kun for sjov

Disse notebooks her er egentligt ment som lidt sjov indlæring I hvad man kan lave af sjove ting i Python og Jupyter Notebooks.

## Dude where is my car?

![alt Dude where's my car](https://64.media.tumblr.com/tumblr_lq1wrnrALQ1r1uduuo1_500.gif)

Var en sjov lille [notebook](Wheresmycar.ipynb), jeg lavede som noget af det første.  
Jeg var oprindeligt hos [:Dribe](https://http://www.dribe.dk/), hvor jeg var så heldig at have en firmabil.  
Når disse firmabiler bliver solgt igen, så bliver de oftest solgt gemmen [Semler Mobility](https://www.semlermobility.dk/), hvis de da ikke eksporteres.

Derfor lavede jeg denne lille notebook, for at holde øje med, hvornår den blev sat til salg (og evt. hvilken pris).

Bilen er for længst solgt, det tog kun otte dage, men jeg kan her vise lidt af prosssen for, hvordan jeg fandt de data jeg skulle bruge.

Først gik jeg ind på hjemmesiden, udfyldte mine søge kriterier, åbner developer tool, og kigger specielt efter `xhf` (læs evt. selv mere om [XMLHttpRequest](https://en.wikipedia.org/wiki/XMLHttpRequest)) i `network settings`.  
Trykker på søg, og finder så den side og resultat der laver listen. 
Denne liste kan jeg så vælge at få kopieret som et cURL script.

Dette kopieret cURL script, kan jeg så tage med over i mit andet farvoritværktøj - [Postman](https://www.postman.com/). 
I Postman kan jeg så simpelthen paste de før kopieret cURL script ind, og så kan jeg begynde at tilpasse mit kald til dette api.  
Når jeg er tilfreds med resultatet, så kan jeg få Postman, til at give mig et eksempel på, hvordan dette kald så kan laves i Python.

Det er så det jeg har brugt som udhangspunkt i [notebooken](Wheresmycar.ipynb), jeg har dog i dette tilfælde valgt at omsrkice det til at bruge et andet http bibliotek end det standard der er foreslået af Postman, da `httpx` har lidt flere settings at vælge imellem.

## Hedder du også Thomas?

En af de andre kuriøse småting jeg har brugt Python til, var at skrabe vores SuccessFactors portal for alle ansatte.

Da jeg kom til Group Data Analytics, så startede jeg samtidigt med en Thomas.  
Vores chef hedder Thomas, og hans chef hedder *også* Thomas.

Så er **Thomas** det mest populære navn i Semler?  
Det var det jeg forsøgte at finde ud af med denne [notebook](./HedderDuThomas.ipynb).