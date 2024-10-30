# Algebra-Relazionale

>- Insiemi:
>    - Unione `U`
>    - Intersezione `A`
>    - Differenza `-`

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
| Join | JOIN | -  | $`PROJ _{lista \quad attributi} (Operando \quad JOIN _{@1 = @2} \quad SEL \quad _{@3>X} \quad (Operando))`$ |

>[!NOTE]
>$`PROJ _{Nome, Cognome} (SEL _{eta > 50} (Persone))`$

### Cardinalità delle proiezioni
se `X` è superchiave di R , allora  $`PROJ _X (R)`$ contiene esattamente R ennuple.
### Select e Null
$`SEL _{@ > X \quad OR \quad @ \leq X} (Opearando) \neq Operando`$ - `IS NULL` oppure `IS NOT NULL`
