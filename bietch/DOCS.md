# BIETCH

## Installeren

1. Voeg `https://github.com/Allardo24/bietch-ha` toe bij de repositories van de Home Assistant-addonwinkel.
2. Installeer BIETCH, schakel starten bij opstarten in en start de addon.
3. Open `http://<IP-van-je-Pi>:8097` of klik op de webinterface-knop. Maak je eigen BIETCH-account en groep aan.
4. Zet in de bestaande Cloudflared-addon het hostname `bietch.allardnet.nl` door naar `http://<IP-van-je-Pi>:8097`.

De server draait lokaal op de Pi, net als Binga. Cloudflared verzorgt de externe HTTPS-toegang. Er zijn geen HA-accounts nodig voor groepsleden. Uitnodigingslinks en QR-codes gebruiken automatisch `https://bietch.allardnet.nl`, ook als de penningmeester de app lokaal opent.

## Updates en gegevens

Dubbelklik op je ontwikkel-pc op `publiceer-ha.bat`, vul je versienummer in en laat het venster open. De starter publiceert zelfstandig via GitHub en biedt de HA-update pas aan als het versie-image beschikbaar is. Er draaien alleen eenvoudige controles, geen browsertests. Vernieuw daarna de HA-winkel en installeer de update. De versie is zichtbaar in BIETCH naast het logo.

De database staat in `/data/bietch.sqlite`. Deze gegevens blijven behouden bij updates en herstarts. Maak een HA-backup voor updates; BIETCH wordt tijdens een backup kort gestopt zodat SQLite consistent wordt opgeslagen. De bestaande gegevens op je Windows-ontwikkelserver worden niet automatisch overgezet naar de Pi.

## Import en retrieve

Je kunt specificaties uploaden vanuit BIETCH. De externe retrieve-code draait afzonderlijk en wordt niet door deze addon uitgevoerd. Stel per groep een retrievesleutel in onder Aanvoer & import. De server slaat geen bronwachtwoorden op. De ontwikkelaar vindt `RETRIEVE-CONTRACT.md` in de private bronrepository voor de koppeling.

De broncode staat privé in `Allardo24/bietch`. Deze openbare repository bevat alleen de HA-catalogus; het gepubliceerde server-image bevat geen bronrekeningen of accountgegevens.
