# **NLG - Developer Applicatie**

---

### :pushpin: Voor wie: Onervaren developers

Hey,

Leuk dat je interesse hebt in developen bij NLG! :computer: Hier krijg je een korte opdracht om mee te beginnen. Je hoeft nog niks te kunnen — we leggen alles stap voor stap uit. Ik verwacht screenshots in mijn DM over een week! :smile:

Veel plezier! :muscle:

- Rebecca // Ragbecca
- Marten // Marten_mrfcyt

_En onthoud: fouten maken hoort erbij!_ :sunglasses:

---

## :white_check_mark: Opdracht 1: Hello World

1. **Download IntelliJ IDEA (Community Edition)**
:point_right: [Download hier](https://www.jetbrains.com/idea/download/?section=windows)

2. **Maak een Java-project aan**
:point_right: [Volg deze stappen](https://www.jetbrains.com/help/idea/creating-and-running-your-first-java-application.html#get-started)

> Zet "Add Sample Code" **uit** tijdens het maken!

3. **Zorg dat je een JDK installeert** als je dat nog niet hebt.

---

### :brain: Uitleg over Java

**Wat is een class?**
> Een class is een soort container voor code. Bijvoorbeeld: `FruitTypes` kan een class zijn waarin je fruitsoorten opslaat.

**Wat is de `main`-methode?**
> De motor van je programma. Alles start vanuit hier.

```java
public class HelloWorld {
    public static void main(String[] args) {
        HelloWorld plugin = new HelloWorld();
    }
}
```

**Wat betekent alles in `public static void main(String[] args)`?**

- `public` = iedereen mag deze functie gebruiken
- `static` = je hoeft geen object aan te maken om het te gebruiken
- `void` = het geeft niks terug
- `main` = de naam van de methode
- `String[] args` = een array van strings (gegevenslijstje)

**Voorbeeld array:**

```java
public class HelloWorld {
    public static void main(String[] args) {
        String[] fruits = {"banana", "orange", "lemon"};
        System.out.println(fruits[0]); // banana
    }
}
```

### :sparkles: Jouw opdracht:
- Maak een grote `String[]` array (geen fruit)
- Print de eerste waarde
- Print de laatste waarde (zonder expliciet indexnummer)
- Kies een thema

---

## :rocket: Opdracht 2 (niet verplicht)

Je leert nu extra over objecten, functies, beveiliging, arrays en nog veel meer!

### :sponge: Limitatie van Arrays

Arrays kunnen niet groter worden:

```java
public static void main(String[] args) {
    String[] fruits = {"banana", "orange", "apple"};
    fruits[0] = "pear";
    System.out.println(fruits[0]); // pear
    // fruits[3] = "kiwi"; // ERROR: Index out of bounds!
}
```

### :electric_plug: Wat is een package?
> Een soort gereedschapskist voor Java. Sommige dingen zoals `String` hoef je niet te importeren, andere wel.

**Een compiler zet je code om naar iets wat de computer snapt.**

### :bricks: Interface + Implementatie

```java
interface Fruit {
    String name = "Fruit";
    void showName();
}

class Apple implements Fruit {
    @Override
    public void showName() {
        System.out.println(name);
    }
}
```

:arrow_right: Met `@Override` pas je een methode aan.  
:arrow_right: `implements` geeft aan dat je een interface gebruikt.

---

## :books: Wat is een `List`?

Een List is als een array, maar dan flexibel.

```java
import java.util.List;
import java.util.ArrayList;

public class HelloWorld {
    public static void main(String[] args) {
        List<String> lijst = new ArrayList<>();
        lijst.add("hallo");
        lijst.remove(0);
    }
}
```

:arrow_right: `new` betekent dat je een nieuw object maakt en geheugen reserveert  
:arrow_right: `<String>` geeft aan wat voor type data de lijst bevat

> Alternatief:
```java
List<String> lijst = List.of("hallo", "wereld");
```
Let op: deze is niet aanpasbaar!

### :blue_book: Meer info:
:point_right: [ArrayList JavaDoc](https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html)

---

### :sparkles: Opdracht 2 Taken:

- Leg uit wat een `int` is
- Noem andere datatypes
- Maak een lijst (zelfde thema als opdracht 1)
- Print eerste en laatste waarde van de lijst
- Maak de lijst leeg, print de lengte (moet 0 zijn)

---

## :rocket: Opdracht 3 (niet verplicht)

Je leert nu extra over datatypes, variabelen en aanpassingen van datatypes

### :one: Nummer DataType

Een int kan alle verschillende getallen tussen -2.147.483.648 en 2.147.483.647 dit is een 32-bit getal
Een long kan meer, deze is namelijk 64-bit. (Dus een maximaal getal in een quintiljoen)
Een short is 16-bit
Een byte is 8-bit

### :two: Komma-getal DataType
:negative_squared_cross_mark: Een komma-getal kan niet opgeslagen worden in een int maar wel in een float (32-bit) en een double (64-bit)

### :three: Extra DataTypes
- char ('c' een enkele letter of andere teken)
- boolean (true of false, is er om te kijken of iets waar of niet waar is)

#### :question: Wist je dat?
Een String niks anders is dan een char-array?

---
### :exclamation: Voorbeeld

```java
byte ditIsEenByte = 1;
short ditIsEenShort = 128;
int ditIsEenInt = 32768;
long ditIsEenLong = 32768L;
float ditIsEenFloat = 12.2F;
double ditIsEenDouble = 12.2;
char ditIsEenChar = 'x';
boolean ditIsEenBoolean = false;
```

#### :question: Zie je?
Dat long en floats een suffix hebben? Die moeten namelijk een L (of l) en F (of f) aan het einde hebben, want anders worden ze geregisteerd als int (alleen als het kort genoeg is) of double

### :rocket: Van 1 DataType naar de ander
Datatypes kunnen naar andere datatypes veranderd worden, van kleiner naar groter kan altijd! Maar van groter naar kleiner moet gecast worden! Want misschien past het er niet in!
> Wat is casten? Casten is zeggen teggen iets: het is nu A maar het moet eigenlijk B zijn. Als dit niet lukt krijg je een waarschuwing of error 'Cannot cast 'B' to 'A''
```java
short byteNaarShort = ditIsEenByte;
int shortNaarInt = ditIsEenShort;
long intNaarLong = ditIsEenInt;
double floatNaarDouble = ditIsEenFloat;
```

Nu met casting
```java
long kleineLong = 1L;
int longNaarInt = (int) kleineLong;
short intNaarShort = (short) longNaarInt;
byte shortNaarByte = (byte) intNaarShort;

double kleineDouble = 12.2;
float doubleNaarFloat = (float) kleineDouble;

int kleineInt = 120;
char intNaarChar = (char) kleineInt; // Wordt een 'x'
```
> Om te zien welke chars welke int-waardes hebben bekijk: [ASCII](https://www.w3schools.com/charsets/ref_html_ascii.asp)

### :postbox: Variabele aanmaken
> 'type' 'variabeleNaam' = 'waarde';
> Een type is bvb een String of een int

#### :exclamation: Een variabele-naam verzinnen
Er zijn veel opties om een naam te verzinnen. [Hier kan je de regels vinden](https://www.w3schools.com/java/java_variables_identifiers.asp)
> Normale regels voor het maken variabelen kan je vinden op de website van Oracle (Makers van Java) [Klik hier](https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html)

### :sponge: Aanpassen van een datatype variabele
Het is mogelijk om een datatype variabele aan te passen. Je hebt de opties:
- `+` (of +=) plus
- `-` (of -=) min
- `*` (of *=) keer
- `/` (of /=) gedeeld door
- `%` (of %=) modulus, wat er overblijft als je / doet

```java
int voorbeeldInt = 10;
voorbeeldInt = voorbeeldInt + 10; // 20
voorbeeldInt += 10; // 30
voorbeeldInt = voorbeeldInt - 5; // 25
voorbeeldInt -= 5; // 20
voorbeeldInt = voorbeeldInt * 2; // 40
voorbeeldInt *= 2; // 80
voorbeeldInt = voorbeeldInt / 2; // 40
voorbeeldInt /= 2; // 20
```

---

### :sparkles: Opdracht 3 Taken:

- Maak een `long`
- Maak een `float`
- Maak een `int array`
- Maak een `Integer List`
- Voor alle 4 de aangemaakte variabelen doe dit:
    - Maak het getal groter
    - Maak het getal kleiner
    - Deel het getal door 2 (Zonder het datatype te veranderen)
    - Keer het getal met 4
    - Verkrijg de modulus van 3
    - Print elke waarde elke keer uit
 
---

## :rocket: Opdracht 4 (niet verplicht)

Je leert nu wat meer over booleans en if-statements

**Wat is een boolean?**
> Een ja of nee antwoord

### :sponge: Wat kan je met een boolean?
Een vraag beantwoorden! Doormiddel van een `vergelijking`!

### :exclamation: vergelijking
Een vergelijking kan je op verschillende manieren creëren
```java
boolean b1 = 5 > 6; // false, 5 is niet groter dan 6
boolean b2 = 5 < 6; // true, 5 is kleiner dan 6
boolean b3 = 6 == 6; // true, 6 is hetzelfde als 6
boolean b4 = 5 != 6; // true, 5 is niet hetzelfde als 6 en dat is gevraagd
```

### :question: Waarvoor gebruik je een boolean?
Een boolean gebruik je dus om iets te vergelijken! Maar om dat echt te gebruiken heb je meerdere opties, 2 leren we je nu:
- if-statements
> Is iets waar, doe dit
- ternary operators
> Is iets waar, geef dit anders de andere optie

**Hoe ziet dat er dan uit?**
If-statement
```java
int i = 0;
int j = 1;
if (i > j) {
// Komt hier nooit in want i is niet groter dan j
}
```

Uitgebreide if-statement :fire:
```java
int i = 0;
int j = 1;
if (i > j) {
// Komt hier nooit in want i is niet groter dan j
} else if (i == j) {
// Komt hier nooit in want i is niet hetzelfde als j
} else {
// Komt hier wel in, omdat dit de prullenbak is die alles pakt wat nog overblijft!
}
```
> If is dus een waar of nietwaar vraag die een boolean vraagt
> Else-if is een extra optie na de if, waarbij iets nieuws wordt vergeleken maar als de if al waar is, wordt dit **nooit** vergeleken
> Else is de prullenbak, hier komt alles in wat niet door de voorgaande (else-)if's komt

Ternary operator :grey_question:
```java
String value = 6 > 5 ? "Waar" : "Niet Waar"; // Wordt "Waar" want 6 is groter dan 5
```
> Wordt gebruikt als er een a of b optie gegeven moet worden door een boolean-vergelijking
> Opmaak: <vergelijking> ? <alsTrue> : <alsFalse>;

---

### :sparkles: Opdracht 4 Taken:

- Maak een `if-statement` die:
    - Kijkt of 2 waardes gelijk zijn, en dan 1 print
    - Kijkt of 1 van de 2 waardes groter is, en dan 2 print
    - Resterend, en dan 3 print
- Maak 2 `Strings`
    - Vergelijk de 2 Strings in een ternary-operator
    - Print de waarde die je hebt verzonnen voor true (of false, hangt van je 2 Strings af)
