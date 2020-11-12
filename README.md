# Vi lär oss IPFS!

IPFS, Inter-Planetary File System, är ett distribuerat system för att spara och hämta filer, webbsidor, applikationer, och data. Jag har fått lära mig lite om det under mitt nuvarande uppdrag, och tror att det kommer vara ett viktigt nästa steg i hela internets vidare framgång. 

## Takeaways
Jag tror du kan tjäna på att ta en timme och labba med grunderna för IPFS för att:
 * få lite inblick i hur internet kan komma att utvecklas
 * utmana din förståelse av hur internet funkar (och hur det skulle kunna funka istället)
 * testa på spännande frmatidsteknologi medan den fortfarande är i ett väldigt tidigt stadium

Om du redan är övertygad, börja med att läsa på lite grann! 
https://ipfs.io/
https://docs.ipfs.io/concepts/what-is-ipfs/

## Mål
Under den här labben kan du åstadkomma följande:
 [] 1. Ladda ner en fil genom IPFS utan att ens installera nånting.
 [] 2. Installera IPFS så din dator kan prata med nätverket direkt.
 [] 3. Se ett axplock på noder i världen som din klient interagerar med, peer-to-peer!
 [] 4. Gör en egen fil tillgänglig, och dela länken till filen!
 [] 5. Lär dig hur en webbsida skulle kunna fungera genom IPFS

Låter det bra? Då sätter vi igång!

## 0. Definitioner

### CID

Länken till en fil på IPFS kallas för en "CID". Här är ett exempel: `bafybeifx7yeb55armcsxwwitkymga5xf53dxiarykms3ygqic223w5sk3m`
De funkar inte som vanliga länkar vi är vana vid. IP-addresser beskriver platser på internet, men servern på den platsen kan välja att skicka tillbaka vad som helst när du frågar. CID-ar är istället beräknade baserat på själva filens innehåll. `bafybeifx7yeb55armcsxwwitkymga5xf53dxiarykms3ygqic223w5sk3m` är en hash på filen den "länkar till", men den säger faktiskt inget om _vem som har filen_. IPFS tillhandahåller ändå ett system att hitta innehållet så länge någon alls på nätverket har den.

### Nod

En server som "pratar IPFS" med andra servrar på IPFS-nätverket. Genom att fråga sina peers kan den hitta filer som CID-ar beskriver. De flesta webbläsare "pratar inte IPFS", så du kan inte utföra ett anrop mot en nod direkt.

### Gateway

En server som pratar HTTP/S, och agerar proxy så att du kan fråga den om filen bakom en CID du tillhandahåller. Gatewayer finns för att folk med vanliga webbläsare ska kunna öppna länkar till IPFS.

## 1. Ladda ner en fil

Första utmaningen! Här är en länk till en bild på en gullig katt: `Qmd286K6pohQcTKYqnS1YhWrCiS4gz7Xi34sdwMe9USZ7u`. Tyvärr kan din webbläsare nog inte öppna länken. Frukta icke! Använd (https://ipfs.github.io/public-gateway-checker/)[denna lista på publika IPFS gateways], och försök luska ut hur du ska använda dem för att ladda ner bilden. Tänk på att inte alla gatewayerna i listan är helt fungerande.

När du kan se bilden är du redo att gå vidare. 

## 2. Installera 

Visst var katten gulligt? Men du kan inte lista på folks välgörenhet för att kunna öppna IPFS-länkar, utan du vill kunna nå dem själv. 
Installera IPFS Desktop och ta saken i egna händer: https://docs.ipfs.io/install/ipfs-desktop/ 
Om du föredrar att lägga tid på att leta upp konsollkommandon, är terminalvarianten kanske tillräcklig: https://docs.ipfs.io/install/command-line/

När du lyckas hämta samma bild genom din nyinstallerade mjukvara är du redo att gå vidare.

## 3. Dela själv

Alla kan dela filer! Välj en egen fil, kanske helst en liten textfil till att börja med om du vill att saker ska gå snabbt, och 




