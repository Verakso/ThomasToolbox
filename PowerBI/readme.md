# PowerBI

Hos Semler har vi mere en 100 forskellige workspaces.  
Det tager noget tid at åbne hver enkelt og løbe dem igennem, så da jeg have brug for et hurtigt overblik over alle vores modeller, kikkede jeg ind i et API til dette.

## Get Data From Workspaces

Er en [notebook](./GetDataFromWorkspaces.ipynb) der:

1. Løber alle de workspaces igennem man har adgang til
2. Henter i hvert workspace
    1. Alle rapporter
    2. Alle dataset
3. Gemmer et udtræk af de funde oplysninger i `Excel`

I denne notebook har jeg valgt at bruge `InteractiveBrowserCredential`, dvs. at når man køre denne workbook, så åbner den ens browser, og man logger så på https://api.powerbi.com med sine egne credentials, og får et token der så bruges til de resterende kald.  
Dette kan laves om hvis man ønsker det, til at bruge et decideret token man laver Azure portalen, men det kræver nogle specifikke rettigheder, men det er mere hvis man fil fuldstændigt automatisere denne dele

---

Hvad kan det så bruges til?

Jo, altså ud over man nemt og hurtigt kan trække nogle lister ud af ens PowerBI miljø for at få et bedre overblik, så kunne man eks. forestille sig et scenarie, hvor man eksempelvis løber alle workspaces igennem og finder de dataset der ikke er opdateret, og så kunne man trigge en opdatering (også gennem API'et).

I sidste ende, er de jo kun ens fantasi der sætter en begrænsning :smirk: