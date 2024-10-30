# Algebra-Relazionale

>- Insiemi:
>    - $` \bigcup `$ - Unione
>    - $`\bigcap`$ - Intersezione 
>    - $`-`$ - Differenza 

>- Specifici: 
>    - Ridenominazione
>    - Selezione
>    - Proiezione

>- ~~Aggregazione~~
>- Join

***
>[!TIP]
>*I risultati sono relazioni, e le relazioni sono insiemi.*

>[!WARNING]
>**Operando = Table**

| Operazione | Standard | Alternative | Esempio |
| :--: | :-- |  :-- | :-- |
| Ridenominazione | REN | $`\rho`$ - *"RHO"*  | $`REN _{genitore <- padre} (Paternità)`$ |
| Selezione | SEL | $`\sigma`$ - *"SIGMA"*  | $`SEL _{condizone} (Operando)`$ |
| Proiezione | PROJ | $`\pi`$ - *"PI"*  | $`PROJ _{lista\quad attributi} (Operando)`$ |
| Join | JOIN | $`\bowtie `$ - *"???"* | $`PROJ _{lista \quad attributi} (Operando \quad JOIN _{@1 = @2} \quad SEL \quad _{@3>X} \quad (Operando))`$ |
| Vista | @ = <...> | $`=`$| $`X = PROJ _{lista \quad attributi} (Operando \quad JOIN \quad Operando)`$ |

>[!NOTE]
>$`PROJ _{Nome, Cognome} (SEL _{eta > 50} (Persone))`$

>### Cardinalità delle proiezioni
>se `X` è superchiave di R , allora  $`PROJ _X (R)`$ contiene esattamente R ennuple.

>### Select e Null
>$`SEL _{@ > X \quad OR \quad @ \leq X} (Opearando) \neq Operando`$ - `IS NULL` oppure `IS NOT NULL`

>[!CAUTION]
>## Cardinalità del join ($`R_1 \quad e \quad R_2`$)
>$` 0 \leq |R_1 \bowtie R_2| \leq |R_1|*|R_2| `$ <br>
>Usando il vincolo di integrità, ovvero le foreign key/ le referenze (2.2 - p78?) <br>
>
>$`R_1(A,B) , R_2(B,C) \quad \to \quad |R_1 JOIN R_2| = |R_1|`$ <br>
> dove `B` vincolo di integrità

>[!WARNING]
>### Join esterno
>- left
>- right
>- full
>
> Lasciano dei null nelle correlazioni mancanti
>
> $`R_1(X_1) , R_2(X_2) \quad \to \quad PROJ_{X_1} (R_1 JOIN R_2) \subseteq R_1`$ <br>
> $`R(X) , X = X_1 \bigcup X_2  \quad \to \quad (PROJ_{X_1} (R)) JOIN (PROJ_{X_2} (R)) \supseteq R`$ <br>
> Uguaglianza quando gli attributi sono in comune alle due proiezioni (Basta la superchiave di una delle 2 proiezioni)

>[!CAUTION]
>### Prodotto cartesiano
>Join naturale (no null) <br>
>***Theta-join*** $`SEL_{condizone}(R_1 JOIN R_2)`$ <br>
>***Equi-join*** quando l'operatore di confronto è sempre uguaglianza. <- Importante
