# Teknisk Dokumentationsrapport

## Introduktion

Denne rapport giver en oversigt over de forskellige komponenter og funktioner, der er tilgængelige i Kulturnat-projektet. Projektet er struktureret ved hjælp af Astro, et moderne statisk site generator framework. Dokumentationen beskriver funktionerne af komponenterne i components-mappen og fremhæver de generelle typografier og stylinger, der anvendes i projektet.

Indholdsfortegnelse

1. Oversigt
2. Komponenter

- URL knapper
- FilterButton
- FilterClick
- FilterSystem
- Footer
- Interaktiv gradient-knap-komponent
- Hero
- ImageBorder
- Newsletter
- Partners
- Program komponenter
- SoMe

3. Sider

- Index
- Program

4. CSS
5. Astro

- Komponenter og layout

6. Logo
7. Konklusion

## Oversigt

Projektet er struktureret i følgende mapper og filer:

- components/: Indeholder genanvendelige komponenter.
- layouts/: Indeholder layoutfiler.
- pages/: Indeholder siderne på hjemmesiden.
- assets/: Indeholder billeder og SVG-filer.
- styles/: Indeholder CSS-filer.

## Komponenter

Projektets formål har været at arbejde med astro og lære, hvordan man laver komponenter man kan genanvende flere gange. Her er et udsnit af forskellige komponenter som der har været fokus på, eller har gentaget sig i projektet:

### URL knapper

ButtonGreen & ButtonRed er komponenter, der viser en farvet knap. Den bruges til at fremhæve links/genveje, som brugeren kan udføre, såsom at læse mere om Kulturnat eller blive arrangør. Knapperne er stylet med en baggrundsfarve og farvet tekst.

### Filter komponenter

Vores filter system er lavet af flere forskellige komponenter.
FilterButton er et komponent, der viser en knap til filtrering af indhold. Den bruges i forbindelse med FilterSystem-komponenten til at give brugeren mulighed for at filtrere aktiviteter og begivenheder baseret på forskellige kriterier.

FilterClick er et komponent, der håndterer klikbegivenheder for filtreringsknapper. Den bruges sammen med FilterButton og FilterSystem for at give en interaktiv filtreringsoplevelse.

FilterSystem
FilterSystem er et komponent, der indeholder logikken og UI-elementerne til filtrering af aktiviteter og begivenheder. Den giver brugeren mulighed for at vælge forskellige filtre og se de relevante resultater.

### Footer

Footer viser kontaktoplysninger og sociale medie-links. Den indeholder også en tilmeldingsformular til nyhedsbrevet og en liste over partnere af projektet. Footer-komponenten er stylet med en grid-layout for at organisere indholdet i to kolonner.

### Interaktiv gradient-knap-komponent

H1Button viser en overskrift med en knap, som aktivere ændringen af farvene i en gradient, for at illustrere overgangen fra dag til nat. Moon er en dekorativ komponent, der viser en måne. Den bruges til at tilføje visuel interesse til siden og understøtte temaet for Kulturnat.

### Hero

Hero er et komponent, der viser en hero-sektion øverst på siden. Den indeholder et billede og en nedtælling til Kulturnat. Hero-sektionen er stylet med en stor baggrundsbillede med dekorativ ramme.

### ImageBorder

Ligsom Hero komponentet, er ImageBorder et komponent, der viser et billede med en ramme. Billedet og rammen er positioneret ved hjælp af absolut positionering og z-index.

### Newsletter

Newsletter - et komponent der viser en tilmeldingsformular til nyhedsbrevet. Den giver brugeren mulighed for at tilmelde sig nyhedsbrevet og modtage opdateringer om Kulturnat. Formularen er stylet med inputfelter og en send-knap. Efter aktivitet på send-knappen, opstår en tekst for bekræftelse.

### Partners

Partners viser en liste over partnere. Den bruges til at fremhæve de organisationer og virksomheder, der støtter Kulturnat. Partnerne er vist i et flex-layout for at organisere dem pænt på siden og sat i en rulle-bånds effekt med javascript.

### Program komponenter

ProgramList er et komponent, der viser en liste over aktiviteter og begivenheder. Den bruges til at organisere og vise programmet for Kulturnat i en overskuelig liste. Listen er stylet med marginer og padding for at adskille elementerne.

ProgramCard er et komponent, der viser et kort med information om en aktivitet eller begivenhed. Den indeholder en titel, en beskrivelse og et billede. Kortene er stylet med en ramme og en skygge for at give dem en kortlignende udseende.

ProgramButton viser en knap med en baggrundsfarve og et ikon. Den bruges til at fremhæve forskellige sektioner af programmet for Kulturnat. Knapperne er stylet med en rund form og en farve, der kan tilpasses via komponentens props, og skiftes med "+" og "-" ikoner.

### SoMe

SoMe viser et ikon og et link til en social medieprofil. Den bruges i Footer-komponenten til at give brugeren mulighed for at følge Kulturnat på sociale medier. Ikonerne er stylet med en ensartet størrelse og farve. Den indeholder også ikonet fra Kultunaut, som er ejerene af Kulturnat.

## Sider

index.astro er hovedsiden for projektet.
program.astro er en side, der viser programmet for Kulturnat.

Begge sider er bygget op ud fra Layout.astro, som indsætter den nødvendige HTML struktur, hvor alt indholdet fra siderne indsættes i slot-sektionen

## CSS

generel.css indeholder generelle stilarter for projektet. Her er nogle af de vigtigste typografier og stylinger:

- Global reset: Alle elementer er sat til box-sizing: border-box for at sikre ensartet padding og margin.
- Farvevariabler: Projektet bruger CSS-variabler til at definere farver, såsom --primary_darkgrey, --secundary-pink, --secundary-oat og --accent.

### Typografi

Typografien i projektet er defineret for forskellige HTML-elementer som h1, h2, h3, og p. Her er en beskrivelse af, hvordan disse elementer er stylet:

### Overskrifter

Overskrifter (h1, h2, h3) bruges til at strukturere indholdet og give visuel hierarki.

- h1: Anton, str. 72.
- h2: Neue Haas Grotesk Display Pro, bold, str. 24.
- p: Neue Haas Grotesk Display Pro, light, str. 24.

## Astro

Vi er netop blevet introduceret for astro i dette forløb. Astro er designet til at bygge hurtige, statiske hjemmesider.

### Komponenter og layout

#### Komponenter

I Astro er en komponent en genanvendelig fil med .astro-endelse. Den fungerer som en separat byggeklods, ligesom det bruges i Figma.

#### Layout

Et layout er en speciel type komponent, der bruges til at strukturere sider og genbruge fælles elementer. Eksempelvis et head-element og body.

#### Slots

Slots bruges til at indsætte dynamisk indhold i en komponent. Det er sektionen, hvor det indhold man vil indsætte inde for vinkelparenteserne.

#### Props

Const bruges sammen med Astro.props til at modtage og bruge props (egenskaber) i en komponent. Props gør det muligt at sende data fra en forælder-komponent eller en side til en anden komponent. Det er en måde for komponenter og sider at kommunikere og sende data.

## Logo

Vores logo er udarbejdet i Adobe Illustrator. Det er inspireret af det nuværende logo fra Kulturnat Helsingør, men med vores eget twist.
Vi beskriver det som:
Abstrakt, måne, hav, ham der fisker fra dreamworks filmene. Eventyrligt. Flyver den eller er det en bølge? Symbolsk

## Konklusion

Denne dokumentation giver en grundlæggende oversigt over de forskellige komponenter og funktioner, der er tilgængelige i Kulturnat-projektet, samt en dybdegående beskrivelse af de generelle CSS-stilarter, der anvendes på tværs af projektet. For mere detaljeret information, besøg venligst de relevante filer og mapper i projektet.
