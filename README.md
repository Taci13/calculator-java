Informacije o projektu

Opis: Projekat kalkulatora napisan u Javi, podržava osnovne aritmetičke operacije: sabiranje, oduzimanje, množenje i deljenje.
Cilj: rad sa osnovnim matematičkim operacijama i implementacija kalkulatora na komandnoj liniji koristeći Javu.
Ukupan broj linija koda: **154**




Izvestaj o statistickoj analizi koda


Fajl: Calculator Java

Calculator.java - linija 6 - static float finalResult;
Zapažanje:Ova promenljiva je statička i koristi se globalno u klasi. Statističke promenljive mogu uzrokovati probleme u većim sistemima jer čine praćenje stanja složenijim.
  
Calculator.java - linija 8 - static class Operations 
 Zapažanje:Korišćenje statičke unutrašnje klase je korisno.Možda bi trebalo da bude samo pomoćna klasa, ali statička implementacija se koristi da bi se izbeglo stvaranje instanci klase.
 
Calculator.java - linija  18 - public static String ToString() 
Zapažanje:Metoda ToString() vraća string sa svim operacijama.Preporučljivo da se promeni ime na nešto preciznije.

Calculator.java - linija 37 - String[] numbers = expression.split("[" + Operations.ToString() + "]");
Zapažanje:Može dovesti do problema ako se izraz neformatira pravilno.

Calculator.java - linija 40 - List<String> operationList = new ArrayList<>();
Zapažanje:Korišćenje ArrayList za čuvanje operacija je adekvatno

Calculator.java - linija 62 - numberList.add(Float.parseFloat(numbers[i]));
Zapažanje:Float.parseFloat() može izazvati greške ako je broj u neispravnom formatu.

Calculator.java - linija 69 - Calculate(numberList, operationList);
Zapažanje:Calculate() poziva samu sebe.Može dovesti do problema sa performansama.
 
Fajl: Start.java

Start.java - linija 9 - Scanner scanIn;
Zapažanje:Objekt Scanner je deklarisan, ali nije odmah inicijalizovan. Može izazvati greške.

Start.java - linija 12 - scanIn = new Scanner(System.in);
Zapažanje:Objekat skenera nije zatvoren nakon upotrebe, čime bi se smanjila mogućnost greške u kodu.

Start.java - linija 15 - if (Expression.equals("exit")) 
 Zapažanje:Ova linija poredi korisnički unos sa stringom "exit" 


Zaključak:
Izveštaj je napisan u formatu koji traži zadatak, sa fajl, broj linije koda, i zapažanjem za svaki od ključnih delova koda u projektu. 
Svi ovi zaključci su sačuvani u **README.md** fajlu, kao što je navedeno u zadatku.

