## Introduction

Project **OpenCPLC** ma być otwartoźródłowym projektem linii sterowników **SoftPLC** wraz z modułami rozszerzeń.
Moduły będą programowane w języku **Ansi C**, a w projekcie zostanie przygotowany odpowiedni ekosystem, aby maksymalnie uprościć ten proces.
W projekcie nie będzie żadnej warstwy pośredniej pomiędzy programistą, a procesorem. Chyba że przygotujesz ją sobie sam 😄
Produkt będą wyrużniały:

- **Elastyczność** - Łatwość dostosowania rozwiązania do specyficznych potrzeb aplikacji.
  - Software'owo: Wykorzystanie uniwersalnego, języka progamowania jakim jest C, który jest w stanie zaspokoić potrzeby wielu aplikacji.
  - Haedware'owo: Pełen opis wewnętrznej magistrali wymiany danych, pozwalający na doprojektowywanie własnych modułów rozszerzeń.
- **Niskie koszty** - w porównaniu z klasycznymi PLC. Brak licencji, tańsze urządzenia, a także możliwość optymalizacji kosztów poprzez własną produkcję.
- **Wyższa wydajność** - Lepsze wykorzystanie zasobów systemu poprzez zastosowanie systemu czasu rzeczywistego i wszystkich sztuczek z języka C.

Oczywiście istnieją również zagrożenia dla projektu:

- Początkowy brak zaufania do produktu
- Wymagana debrej znajomość języka C

Na chwilę obecną zaprojektowane są dwa modułu:

- **Modem** - Urządzenie master zapewniające interfejs sieci komórkowy do wymiany danych
- **IO4** - Moduł rozszerzeń zapewniający 4 wyjścia i 4 wejścia cyfrowe

# Modem

![modem](images/modem.png)

📐 Schematy układów [PDF](devices/modem/schema.pdf)
📋 Lista materiałowa [XLSX](devices/modem/bom.xlsx)
🔧 Dokumentacja montażowa [PDF](devices/modem/assembly.pdf)
🧰 Pliki produkcyjne [GERBER](devices/modem/gerber/)

### Uwagi do montażu

- Montaż _(lutowanie)_ kosza na baterię trzeba zrobić na końcu po połączeniu płytek `side` oraz `base`, ponieważ utrudnia to ich montaż.
- Płyt muszą być oczyszczone przed montażem kosza na baterię, ponieważ płaski kosza pęka pod wpływem wielu środków do czyszczenia PCB.
- Montaż taśmy łączącej płytki `base` oraz `prog` należy robić, bez podłączonego zasilania i umieszczonej baterii. Wówczas taśma może spowodować zwarcia/przepięcia, które uszkodzą procesor.

# IO4

![io4](images/io4.png)

📐 Schematy układów [PDF](devices/io4/schema.pdf)
📋 Lista materiałowa [XLSX](devices/io4/bom.xlsx)
🔧 Dokumentacja montażowa [PDF](devices/io4/assembly.pdf)
🧰 Pliki produkcyjne [GERBER](devices/io4/gerber/)