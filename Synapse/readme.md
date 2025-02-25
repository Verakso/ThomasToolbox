# Synapse

Vi bruger stort set Synapse Pipelines til alle vores datatransformationer.

Med lidt over 2.000 pipelines, kan de være noget af et arbejde at gennemgå dem alle, så ved hjælpe af API'et, kan man hente alle pipelines ud.

>**[Pipelines](pipelines.ipynb)** er netop en notebook til at hente alle Synapse pipelines ud i `json` format.  
Netop fordi Synapse pipelines er native `json` så kan vi også nemt læse disse filer og hente egenskaberne ud.
>
> I dette konkrete eksempel, ville jeg gerne finde alle de pipelines der var deaktiveret.

På samme måde kan man også hente alle Linked Services ud:

>**[Linked Services](linked_services.ipynb)** er en notebook der henter alle Linked Services ud i en samlet `json` fil.
>
>Tanken var så her, at man kunne hente Linked Services konfigurationerne fra ens forskellige miljøer, eks. `dev`, `test` og `prod` og så kunne man se om, man havde fået sat miljøerne korrekt op.  
Hvis man nu eks. havde en fejl i ens ARM template, så kunne man jo risikere at overskrive disse connections, når man deployer.