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
- [ ] 1. Ladda ner en fil genom IPFS utan att ens installera nånting.
- [ ] 2. Installera IPFS så din dator kan prata med nätverket direkt.
- [ ] 3. Se ett axplock på noder i världen som din klient interagerar med, peer-to-peer!
- [ ] 4. Gör en egen fil tillgänglig, och dela länken till filen!
- [ ] 5. Lär dig hur en webbsida skulle kunna fungera genom IPFS

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

Första utmaningen! Här är en länk till en bild på en gullig katt: `Qmd286K6pohQcTKYqnS1YhWrCiS4gz7Xi34sdwMe9USZ7u`. Tyvärr kan din webbläsare nog inte öppna länken. Frukta icke! Använd [denna lista på publika IPFS gateways](https://ipfs.github.io/public-gateway-checker/), och försök luska ut hur du ska använda dem för att ladda ner bilden. Tänk på att inte alla gatewayerna i listan är helt fungerande.

När du kan se bilden är du redo att gå vidare. 

## 2. Installera 

Visst var katten gulligt? Men du kan inte lista på folks välgörenhet för att kunna öppna IPFS-länkar, utan du vill kunna nå dem själv. 
Installera IPFS Desktop och ta saken i egna händer: https://docs.ipfs.io/install/ipfs-desktop/ 
Om du föredrar att lägga tid på att leta upp konsollkommandon, är terminalvarianten kanske tillräcklig: https://docs.ipfs.io/install/command-line/

När du lyckas hämta samma bild genom din nyinstallerade mjukvara är du redo att gå vidare.

## 3. Se dig omkring

IPFS desktop har en tabb som heter "peers", där du kan hitta andra noder som din nod är medveten om. Hur många pratar du med just nu? Från vilka länder? Finns det några andra från Sverige?

## 4. Dela själv

Alla kan dela filer! Välj en egen fil, kanske helst en liten textfil till att börja med om du vill att saker ska gå snabbt, och hitta ett sätt att dela den med världen genom IPFS. Mjukvaran du installerat tidigare borde ha ett alternativ för det. Hur du än gör, borde du få ut en egen CID. Skicka den till en vän, och se att de kan hämta filen! Som ett exempel är följande en CID till en fil som författaren delar: QmX2WmDCfhP4LGaTSTK51Bp31QsqrPiPqRK7ygrnXnwXyf det är Omegapoints slogan.

När du bekräftat att någon annan kan hämta filen du delar ka ndu gå vidare till nästa steg. Om du inte har någon att dela med, så kan du testa med en public gateway istället från steg 1. De borde lika gärna kunna hitta filen.

## 5. (stretch goal) En länk som kan uppdateras

Länken du skapade är helt baserad på innehållet i filen. Detta passar vissa saker, men om du för en blogg, så kan du inte skicka nya länkar dill folk varje gång du ändrar något! Detta löser HTTP enkelt: servern bakom länken kan när som helst ändra vad den skickar tillbaka. Men det går att lösa i IPFS också. Följande sida har en möjlig lösning: https://docs.ipfs.io/concepts/ipns/

Författaren har inte kommit såhär långt än, so you're on your own. Men om du lyckas skapa en egen address där du kan ändra vad som ligger på den, så får du en guldstjärna!

## Vidare

Ja, denna lilla guide ämnade bara att väcka er aptit. IPFS är på alpha-nivå, det kan kännas som vilda västern och all dokumentation är inte alltid komplett än. De är dock en väldigt aktiv community, och tar emot förbättringar med entusiasm! Så låt din nyfikenhet leda dig, om du ser några fel, rätta dem på github, och dela med dig av det du lär dig! Det finns en hel ocean under ytan om man undrar hur allt funkar. Jag önskar glatt läsande och labbande! Och du kanske vill starta en egen nod och låta den snurra, pro bono?






