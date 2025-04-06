# Vecka 15: Router Bootcamp

## Steg-för-steg

### Steg 1: Vanlig React-applikation

Skapa upp ett vanligt React-projekt, där du rensar bort de filer som inte önskas. Skapa sedan mappen *pages* där du lägger filerna *Home.jsx*, *About.jsx* och Contact.jsx. 
Inledningsvis kan du låta alla sidor returnera sitt namn inuti ett *h1-element* (exempelvis ```<h1>Contact</h1>``` osv.).

### Steg 2: Skapa din RouterProvider

Börja med att välja om du vill lägga din *RouterProvider* i *main.jsx* eller i *App.jsx*. Standard är i *main.jsx*, men så länge vi behöver dela på state mellan våra olika sidor så behöver den snarare ligga i *App.jsx* om vi inte har global statehantering. 
För den här övningens skull spelar det ingen roll. 

1. Importera *createBrowserRouter* och *RouterProvider* från *react-router-dom*.
2. Anropa *createBrowserRouter* och spara returen i en variabel som du döper till *router*. Som argument tar *createBrowserRouter* en array bestående av ett objekt per sida i din applikation. Varje objekt tar nycklarna *path* som skall vara den endpoint man behöver skriva in för att ta sig till sidan (ex. "/about"), samt *element* som är den sido-komponent som skall visas.
3. Läs in din *RouterProvider*-komponent, och som props med namnet *router* skickar du med din *router*-variabel.
4. Testa att skriva in dina olika endpoints i adressfältet för att se om det fungerar.

### Steg 3: Felhantering

Skapa filen *Error.jsx* i din *pages*-mapp. Låt den returnera ett *h1*-element med ett felmeddelande. Lägg därefter till nyckeln *errorElement* i ditt översta objekt i ditt anrop till *createBrowserRouter*, som värde skickar du in din nyskapta sida. Testa om det fungerar genomm att skriva in en endpoint i adressfältet som inte existerar i din router.

### Steg 4: Skapa navigation

1. Skapa mappen *components* där du lägger filen *Header.jsx*. Låt den returnera ett *header*-element.
2. Importera *Link*-komponenten från *react-router-dom*.
3. Inuti ditt *header*-element läser du nu in en *Link*-komponent per sida man skall kunna navigera sig till. Notera att du nu behöver både öppnings- och stängningstaggarna. Mellan taggarna skriver du namnet på sidan som länken skall gå till, och i öppningstaggen lägger du till ett *to*-attribut vars värde skall överensstämma med den endpoint som du angav när du skapade routen i din *RouterProvider* (exempelvis ```<Link to="/">Home</Link>```). Testa att klicka på länkarna för att se om navigationen fungerar.

## Barnbiblioteket - Levelup! Denna övning kommer jag att koda upp på onsdag (distans får detta inspelat i efterhand)

I denna övning ska du göra ett bibliotek av barnböcker. Du hittar data om ett antal barnböcker med hjälp av nedanstående API-anrop:
```
GET https://santosnr6.github.io/Data/childrens_books.json
```

Använd dig av `React router` med två vyer, en för alla böcker och en för en detaljerad vy av en bok.

Figmaskiss: https://www.figma.com/file/lm4l7OViUO8ypfQn9IBG91/Mini-Library?node-id=2%3A41

**Funktionalitet**

* Lista alla böcker från APIet
* När jag klickar på en bok ska den visas med mer information [se Figmaskiss](https://www.figma.com/file/lm4l7OViUO8ypfQn9IBG91/Mini-Library?node-id=2%3A41).

