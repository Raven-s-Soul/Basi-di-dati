# Data Manipulation Language

<!-- Teory -->
> [!NOTE]
>> - Dichiarativi (che cosa)
>>    - Le proprietà del risultato
>
>> - Procedurali (come)
>>    - Il risultato
>>    - [Algebra relazionale](./Algebra-Relazionale.md)
>
>- SQL (Structured Query Language)

***

>[!IMPORTANT]
>## SQL
>
> <!-- Operazioni -->
><details>
><summary>Operazioni</summary><br>
>
>> - Interrogazione
>>   - Select
>
>> - modifica
>>   - Insert
>>   - Delete
>>   - Update
></details>

<!--
Notazioni della repository
-->
>[!TIP]
><details>
><summary>Notazioni</summary>
><p align="center" >
>  
>| Operatore | Definzione |
>| :--: | :-- |
>| `@` | Argomento/Attributo |
<!--
| A | B |
| `###` | ### <br> <details> <summary>Example: </summary><br> ### </details> |
-->
></p>
></details>
>

<!--
SQL
-->

| Operatore | Definzione |
| :--: | :-- |
| `select` | Operatore di interrogazione |
| `*` | Seleziona ogni @ |
| `FROM` | Operatore per la selezione della tabella |
| `WHERE` | Operatore per aggiunta di condizione |
| `AND` | Congiunzione di condizioni <br> <details> <summary>Example: </summary><br> where A.@ = B.@ `AND` A.@ > 4 </details> |
| `UNION` | Opeatore di [unione](https://www.simatematica.it/wp-content/uploads/2022/12/image-15.png) insiemistico <br>Approccio insiemistico <br> <details> <summary>Example: </summary><br> select * from A `UNION` select * from B </details> |
| `UNION ALL` | TODO |
| `EXCEPT` | Opeatore di [differenza](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4iwMT5roVJvi8-T0UOeAFv9S9ok2POEFW1Q&s) insiemistico <br> <details> <summary>Example: </summary><br> select * from A `EXCEPT` select * from B </details> |
| `INTERSECT` | Opeatore di [intersezione](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ79kJndGh-1_wvL7iIoLOmBWqhosV_stQiUw&s) insiemistico <br> <details> <summary>Example: </summary><br> select * from A `INTERSECT` select * from B </details> |
| `DISTINCT` | Operatore per evitare duplicati  <br> <details> <summary>Example: </summary> select `DISTINCT` nome from A </details>  |
| `JOIN` | Connessione intra-tabelle <br> <details> <summary>Example: </summary><br> select * from A `JOIN` B `ON` A.@ = B.@ </details> |
| `USING(@)` | Join naturale uso dello stesso nome per lo stesso argomento <br> <details> <summary>Example: </summary><br> select * from A `JOIN` B `USING(@)` </details> |
| `AS` | Operatore di rinominazione <br> <details> <summary>Example: </summary><br> select data `AS` D from A </details> |
| `LEFT/FULL/RIGHT JOIN` | Connessione esterna <br> <details> <summary>Example: </summary><br> select * from A `LEFT JOIN` B using(@) </details> |
| `ORDER BY @` | Operatore di ordinamento alfabetico |
| `like` | Operatore di ricerca stringhe <br> <details> <summary>Example: </summary><br> where nome `like` 'A_d%' <br><br>Spiegazione: inizia per A e d come 3rd carattere  </details> |
| `IS NULL` | @ = NULL/null |
| `COUNT(@)` | Conta le righe |
| `SUM(@)` | Somma delle righe |
| `AVG(@)` | Media delle righe |
| `MAX(@)` | Massimo delle righe |
| `MIN(@)` | Minimo delle righe |
| `<>` | Diverso != |
| `CREATE VIEW <.titolo.> AS` | Creare una view/Gruppo  |
| `GROUP BY @` | Riunisce/ Raggruppa per @ |
| `HAVING AVG(@) > X` | Condizioni sui gruppi  |
| `ANY` | is in ??  |

***

<!-- p100 to check -->

<details>
<summary>I 3 passi</summary>
  
>1) Prodotto cartesiano
>  
>1) Selezione - select
>   
>1) Proiezione - @
</details>

***

## Interrogazioni nidificate

```SQL
Select *
From (...) as X -- any letter can be use as macro of X
Where @ = (select max(@) from Y) -- Uguale
Where @ >= (select avg(@) from Y) -- Maggiore uguale 
```

### Update / Insert / Delete
### Alter table
