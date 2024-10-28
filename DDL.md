# Data Defintion Language

<!--
Create Table Example
-->
<details>
<summary>Create Table Example</summary>
  
```SQL
create table persone(
nome    	character(20) not null primary key,  
eta 	      integer,
reddito     integer
);
create table maternita(
madre    	character(20) not null references persone(nome),  
figlio 	  character(20) not null primary key references persone(nome)
);
create table paternita(
padre    	character(20) not null references persone(nome),  
figlio 	  character(20) not null primary key references persone(nome)
);
```
</details>
