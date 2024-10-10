# 1. INTRODUCCIO

## Per què programar?

En el nostre dia a dia, se’ns plantegen reptes constantment. Durant els anys, aprenem a resoldre aquests reptes, analitzant la situació plantejada i aplicant, de manera sistemàtica, tècniques que ens permeten ser més eficients, segons aquesta situació. És a dir, davant de situacions de la vida quotidiana (fer un tiramisú, jugar a un videojoc, conduir, ...) , seguim instruccions i prenem decisions, en base a certs criteris. 

De manera que si nosaltres realitzem una sèrie de tasques per resoldre el problema, un ordinador haurà de fer el mateix. Com li indiquem? Mitjançant un **programa**.


> Un **programa** és un conjunt d’instruccions (aritmètico-lògiques), executades de manera seqüencial, per tal d’obtenir el resultat esperat.
>
> Una **instrucció** és un conjunt de dades dins d’una seqüència estructurada que el processador interpreta i executa.


# 1.1 Orígens de la programació

La informàtica en general, i la computació en particular, han evolucionat notablement gràcies a la contribució de científics i inventors molt importants. Específicament, en el camp de la programació informàtica, cal posar en rellevància les contribucions de:

 - **[Joseph Marie Jacquard](https://en.wikipedia.org/wiki/Jacquard_machine)**: inventor francès conegut per automatitzar, mitjançant l'ús de targetes perforades, l'anomenat teler de Jacquard.
 - **[Charles Babbage](https://en.wikipedia.org/wiki/Charles_Babbage)**: creador de la màquina diferencial i la màquina analítica (basada en el teler de Jacquard).
 - **[Ada Lovelace](https://en.wikipedia.org/wiki/Ada_Lovelace)**: desenvolupadora de programes per a la màquina analítica de Baggage. A causa d'això va ser considerada la primera programadora de la història. Va ser la primera a utilitzar instruccions condicionals i iteratives, que són la base de la programació actual.
 - **[Alan Turing](https://en.wikipedia.org/wiki/Alan_Turing)**: creador de la màquina de Turing, va treballar en camps com la informàtica teòrica, la criptoanàlisi o la intel·ligència artificial. És considerat el pare de la informàtica moderna.
 - **[Grace Hopper (Amazing Grace)](https://en.wikipedia.org/wiki/Grace_Hopper)**: es va allistar en la marina on va treballar com a programadora en el computador Harvard Mark I. És la creadora del primer compilador i del llenguatge de programació Cobol.


# 1.2 Llenguatges de programació

Les instruccions que conté un programa s’especifiquen mitjançant un llenguatge que l’ordinador pugui entendre. 

![Procés de transformació d’un codi font a un codi executable](/1.2.diagrama_compilacio.jpg)
 - **Codi** font: fitxer o conjunt de fitxers que contenen les instruccions del programa.
 - **Linker**: encarregat d’inserir al codi objecte les funcions de les llibreries que són necessàries per al programa i de dur a terme el procés de muntatge generant un arxiu executable.
 - **Llibreria**: col·lecció de codi predefinit que facilita la tasca del programador a l’hora de codificar un programa.

Un **llenguatge de programació** és un llenguatge que permet establir una comunicació entre l’home i la màquina.

El *codi font* conté (descrits ens un llenguatge de programació concret) els passos que ha de realitzar l’ordinador un cop aquest codi es converteixi en un codi executable.

Els llenguatges de programació es classifiquen:
 - segons el **nivell d’abstracció del llenguatge**
 - segons el **tipus de traducció** del programa al llenguatge màquina

#### 1. Nivells d’abstracció dels llenguatge

Aquesta propietat indica el grau d’abstracció del programa i si les seves instruccions estan més o menys estretament vinculades al funcionament del maquinari d'un ordinador.

Un **llenguatge de programació d'alt nivell** es caracteritza per expressar els algorismes d'una manera adequada a la capacitat cognitiva humana, en lloc de la capacitat amb què els executen les màquines; és a dir, la seva sintaxi s’assembla al llenguatge natural humà. Els llenguatges d'alt nivell poden ser compilats o interpretats. 
 - Com a llenguatges d’alt nivell, tenim C, C++, C#, JAVA i Python, entre d’altres.

En un **llenguatge de programació de baix nivell**, en canvi, les seves instruccions exerceixen un control directe sobre el maquinari i estan condicionats per l'estructura física de les computadores que el suporten. L'ús de la paraula baix en la seva denominació no implica que el llenguatge sigui menys potent que un llenguatge d'alt nivell, sinó que es refereix a la reduïda abstracció entre el llenguatge i el maquinari. Per exemple, aquest tipus de llenguatges s'utilitza per a programar tasques crítiques dels sistemes operatius, d'aplicacions en temps real o controladors de dispositius. 
 - Els llenguatges de baix nivell són el **llenguatge binari i** el **llenguatge assemblador** (la seva abstracció és una mica més elevada).

 ![Nivells d'abastracció dels llenguatges de programació](/nivell_abstraccio_llenguatges.jpg) 
 ![Nivells d'abastracció dels llenguatges de programació. Exemples](/nivells_abstraccio_exemples.jpg)

#### 2. Tipus de traducció dels programes

L'especificació de l’algorisme del programa s'implementa en un llenguatge d’alt nivell, definit en el codi font del programa.  Segons el tipus de traducció a llenguatge màquina, podem classificar els llenguatges com llenguatges compilats o llenguatges interpretats.

Els **llenguatges compilats** tradueixen (compilen) tot el codi font i contenen aquesta traducció en un arxiu executable comprensible per a la màquina en la plataforma en què s'ha compilat. Aquest arxiu pot executar el programa tantes vegades sigui necessari ,sense haver de repetir el procés de compilació. No obstant, l’arxiu només es podrà executar en el mateix sistema operatiu en el que s’ha compilat (Windows, Linux, Mac).
 - Exemples: C, C++, C#, Fortran, Pascal, Haskell i Visual Basic

En canvi, els llenguatges interpretats tradueixen (interpreten) el codi font pas a pas, és a dir, instrucció per instrucció. La traducció del programa es repeteix cada vegada que s'executa el programa. 

Els **llenguatges interpretats** permeten el tipus dinàmic de dades, és a dir, no és necessari inicialitzar una variable amb un determinat tipus de dada, sinó que aquesta pot canviar el seu tipus en condició a la dada que emmagatzema en aquell moment, entre altres característiques més.
 - Python, PHP, JavaScript, Ruby, Perl i MATLAB

![Tipus de traducció dels programes](/traduccio_llenguatges.jpg)

Un cas particular de llenguatge compilat el trobem en el llenguatge JAVA:

1. Tradueix el codi font a un llenguatge intermedi obtenint un programa equivalent amb un menor nivell d’abstracció que l’original i que no pot ser directament executat (fitxer bytecode). 
2. Tradueix el llenguatge intermedi a un llenguatge comprensible per la màquina, fent servir la **JVM** (Java Virtual Machine) específica per al sistema operatiu on s'executa el fitxer que conté el **bytecode** *(.class)*.

![Traducció d'un programa en Java](/media.png)

### Com executa un programa l’ordinador ?

1. S’introdueixen les dades a l’ordinador
2. El processador executa les instruccions
3. Els resultats de les operacions s’emmagatzemen a la RAM
4. Els resultats finals s’emmagatzemen al disc dur

![cpu](/cpu.jpg)

### Com codifica la informació l'ordinador?

Quan treballem amb números, acostumem a treballar en codificació **decimal** (en base 10). L'ordinador, en el seu nivell més baix, treballa en format **binari** (en base 2). No obstant, també farem servir altres tipus de codificacions: **octal** (en base 8) i **hexadecimal** (en base 16).

**Codificació en base 10 (decimal)**. Dígits: 0,1,2,3,4,5,6,7,8,9

345^10^  = 3x10^2^  + 4x10^1^ + 5x10^0^

**Codificació en base 2 (binari)**. Dígits: 0,1

1001^2^ =  1x2^3^ + 0x2^2^ + 0x2^1^ + 1x2^0^ = 91^0^ 

**Codificació en base 8 (octal)**. Dígits: 0,1,2,3,4,5,6,7

743^8^ =  7x8^2^ + 4x8^1^ + 3x8^0^ = 4831^0^ 

**Codificació en base 16 (hexadecimal)**. Dígits: 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F

E7A9^16^ =  14×16^3^ +7×16^2^ +10×16^1^ + 9×16^0^ = 57344+1792+160+9 = 59305^10^

![media](/media.jpg)

#### Conversió de decimal a binari
43^10^ =  101011

![decimal](/decimal-hex~3.jpg)

#### Conversió de decimal a hexadecimal
43^10^ =  2B^16^

En el cas de la codificació de caràcters, es fa servir la taula **ASCII** i la taula **Unicode**, que estandaritzen la relació entre caràcters alfabètics i símbols amb valors decimals.

![Exemple de codificació de la taula ASCII](/ASCII-Table-wide.svg.png)![Exemple de codificació de la taula Unicode](/ascii-code.jpg)

# Classificació dels llenguatges i paradigmes de programació

### 1. Generacions dels llenguatges de programació

Els llenguatges de programació s'han classificat en diverses generacions de llenguatges de programació. Històricament, aquesta classificació s'utilitzava per indicar un poder creixent dels estils de programació. Els escriptors posteriors han redefinit una mica els significats, ja que les distincions anteriorment vistes com a importants es van tornar menys significatives per a la pràctica actual. Actualment es classifiquen en cinc generacions:

**Llenguatge de primera generació**

Correspon al **llenguatge de baix nivell** o **llenguatge màquina**. És màquina-dependent i les sentències del programa s'escriuen en codi binari (0/1).

 - Avantatges:
    1. Ràpid i eficient, ja que les declaracions s'escriuen directament en llenguatge binari.
    2. No cal traductor.
 - Inconvenients:
    1. Dificultat per aprendre codis binaris.
    2. Dificultat d'entendre (el programa i on s'ha produït l'error).

Ex: 000000 10010 10011 10001 00000 100000 *(suma el contingut de dos variables i l'emmagatzema en una tercera)*

**Llenguatges de segona generació**

Són anomenats llenguatges d’**assemblador**. El llenguatge d'assemblador conté notacions llegibles per l'home que es poden convertir en llenguatge màquina utilitzant un assemblador (programa que converteix instruccions d'assemblador a instruccions en llenguatge màquina). Els programadors poden escriure el codi utilitzant codis d'instrucció simbòlics que són abreviatures significatives de mnemonics. També es coneix com a llenguatge de baix nivell.

 - Avantatges:
    1. És més fàcil d'entendre si es compara amb el llenguatge màquina.
    2. Les modificacions són fàcils.
    3. La localització d'errors i la seva correcció són fàcils.
- Inconvenients:
    1. Es requereix un assemblador.
    2. Aquest llenguatge depèn de l'arquitectura /màquina, amb un conjunt d'instruccions diferent per a diferents màquines (depèn de l'arquitectura de l'ordinador).

![Exemple de procés de traducció d'un programa en Assembler](/sentencia-assembler.jpg)

En ser un llenguatge que requereix un ús molt eficient de la velocitat i de la memòria, s'’utilitza per dissenyar drivers.

#### Llenguatges de tercera generació
La tercera generació també s'anomena **llenguatge procedimental** o **llenguatge de programació d'alt nivell**. Substitueixen les instruccions simbòliques per codis independents de la màquina, semblants al llenguatge humà (en anglès) o al de les matemàtiques. Per a l'execució, un programa en aquest lenguatge ha de ser traduït al llenguatge màquina utilitzant un compilador/intèrpret. 

 - Avantatges:
    1. L'ús de paraules semblants a l'anglès el converteix en un llenguatge comprensible per a l'ésser humà.
    2. Requereix un menor nombre de línies de codi en comparació amb els dos llenguatges anteriors.
    3. El mateix codi es pot copiar a una altra màquina i executar-lo utilitzant el compilador específic d'aquesta màquina.
 - Inconvenients:
    1. Cal un compilador/intèrpret.
    2. Es necessiten diferents compiladors per a diferents màquines.

> Exemples d'aquest tipus de llenguatge són C, PASCAL, FORTRAN, COBOL, JAVA, ...

#### Llenguatges de quarta generació

Els llenguatges de quarta generació també s'anomena **llenguatges no procedimentals** o de **propòsit específic**. Aporten un nivell molt alt d’abstracció en la programació, que permet desenvolupar aplicacions sofisticades en un espai curt de temps, molt inferior al necessari per als llenguatges de 3a generació.

 - Avantatges:
    1. Fàcil d'entendre i aprendre.
    2. Es requereix menys temps per a la creació de l'aplicació.
    3. És menys propens a errors.
 - Inconvenients:
    1. El consum de memòria és elevat.
    2. Té un mal control sobre el maquinari.
    3. Menys flexible que els llenguatges de 3a generació.

>Llenguatges de bases de dades: Eines CASE
>Manipulació de dades, anàlisi i informes: R, SPSS
>Llenguatges matemàtics: Matlab

#### Llenguatges de cinquena generació

Els llenguatges de cinquena generació es basen en el concepte d'intel·ligència artificial. En comptes de resoldre un problema algorítmicament, es pot construir una aplicació per resoldre'l basant-se en algunes restriccions, de manera que els ordinadors aprenen a resoldre qualsevol problema.

![Classificació dels llenguatges de programació](/Mapa%20conceptual.png)

 - Avantatges:
    1. Les màquines poden prendre decisions.
    2. L'esforç del programador es redueix per resoldre un problema.
    3. Més fàcil que els llenguatges de 3a o 4a generació per aprendre i utilitzar.
 - Inconvenients:
    1. Codi complex i llarg.
    2. Es necessiten més recursos i també són cars.

> Exemples d'aquest tipus de llenguatge són PROLOG i Lisp.

### 2. Paradigmes de programació

Un **paradigma** de programació consisteix en els mètodes per dur a terme càlculs i en la forma en la qual han d'estructurar-se i organitzar-se les tasques que ha de realitzar un programa. 

Es tracta d'una proposta tecnològica adoptada per una comunitat de programadors i representa un enfocament particular o filosofia per a dissenyar solucions. Els paradigmes difereixen els uns dels altres, en els conceptes i la manera d'abstreure els elements involucrats en un problema, així com en els passos que integren la seva solució del problema.
 - **Programació imperativa o per procediments**
 És el més usat en general i  es basa a donar instruccions a l'ordinador de com fer les coses en forma d'algorismes, en lloc de descriure el problema o la solució. És la forma de programació més usada i la més antiga, l'exemple principal és el llenguatge de màquina. Exemples de llenguatges purs d'aquest paradigma serien **C**, **BASIC** o **Pascal**.

 - **Programació orientada a objectes**
Està basada en el paradigma imperatiu, però encapsula elements denominats objectes que inclouen tant variables com funcions. Es considera **JAVA** com el llenguatge orientat a objectes per excel·lència, però el més representatiu seria **Smalltalk**, que està completament orientat a objectes.

 - **Programació dirigida per esdeveniments**
La programació dirigida per esdeveniments és un paradigma de programació en el qual tant l'estructura com l'execució dels programes van determinats pels successos que esdevenen el sistema, definits per l'usuari o que ells mateixos provoquin. Un exemple d’aquest el trobem en el llenguatge **Visual Basic**.

 - **Programació declarativa**
Està basat a descriure el problema declarant propietats i regles que han de complir-se, en lloc d'instruccions. Hi ha llenguatges per a la programació funcional, la programació lògica (**Prolog**), o la combinació lògic-funcional. La solució és obtinguda mitjançant mecanismes interns de control, sense especificar exactament com trobar-la (tan sols se li indica a la computadora què és el que es desitja obtenir o què és el que s'està buscant). 

 - **Programació multiparadigma**
És l'ús de dos o més paradigmes dins d'un programa. L'objectiu en el disseny d'aquests llenguatges és permetre als programadors utilitzar el millor paradigma per a cada treball, admetent que cap resol tots els problemes de la forma més fàcil i eficient possible. El llenguatge **Lisp** es considera multiparadigma. Igual que **Python** o **PHP** que són orientats a objectes, reflexius, imperatius i funcionals.  **C++​** combina el paradigma imperatiu amb l'orientació a objectes.

# 1.4. els llenguatges de programació més populars

### Quin és el millor llenguatge de programació? 

Segons a qui es pregunti, obtindrem una resposta o una altra. A l’hora d’escollir un llenguatge de programació per a implementar un programa, cal tenir en compte una sèrie de factors:

 - Propòsit del programa
 - Entorn d’execució
 - Versatilitat del llenguatge
 - Tendències del mercat

Tot i de l’existència dels llenguatges multipropòsit, l’opció ideal serà aquella que solucioni, de manera més eficient, el problema plantejat.

A continuació trobareu la llista dels 10 llenguatges de programació més utilitzats (setembre 2024), de tota la llista de **[llenguatges de programació existents](https://www.techrepublic.com/article/tiobe-index-language-rankings/)**.

[![](/AGD15Y99hf-_wYR17jJHW206zALEdQr3kDxMFBwV8v87mryGlLIXHokscsTfiPWy9_YsGEPPfuHX-rJM96PI6cfM-ZhjmlxvW6SX-mqjiUqsLRQFPgSVZm3GGquRSHwJDbIXAE3Dhy7gs60VMm4DyssEY4a0OwgS1hXhMyjTmQ=s2048.jpg)](https://www.techrepublic.com/article/tiobe-index-language-rankings/)
