# Ministerieel besluit van 2005-03-11 houdende goedkeuring van de GRB-specificaties in uitvoering van het decreet van 16 april 2004 houdende het Grootschalig Referentie Bestand

### ART. 1.

De GRB-specificaties, vastgesteld door de stuurgroep GIS-Vlaanderen, in uitvoering van artikel 6 van het decreet van 16 april 2004 houdende het Grootschalig Referentie Bestand en gevoegd als bijlage I bij dit besluit, worden goedgekeurd.

### ART. 2.

Dit besluit treedt in werking op de datum van de bekendmaking ervan in het Belgisch Staatsblad.

## Bijlage I GRB-specificaties, technische bepalingen v1.0 GRB-specificaties, technische bepalingen v1.0

### Tekst

<p>Index<br>
<br>
1. Inleiding<br>
<br>
2. GRB-terminologie<br>
<br>
2.1. Objectgerichtheid<br>
<br>
2.2. Identificatoren<br>
<br>
2.3. GRB-specificaties<br>
<br>
3. Het opmeten van grootschalige geografische gegevens<br>
<br>
3.1. FLEPOS<br>
<br>
3.2. Data-inwinning<br>
<br>
3.2.1. aanmaakspecificaties<br>
<br>
3.2.2. aanmaaktechnieken<br>
<br>
3.2.3. GRB-skeletbestekken<br>
<br>
4. De opname van grootschalige geografische gegevens in het GRB<br>
<br>
4.1. Referentiegegevens<br>
<br>
4.2. GRB-entiteiten volgens de GRB-terreinclassificatie<br>
<br>
4.3. Overzicht thema's en entiteiten van GRB<br>
<br>
4.4. Kwaliteitspecificaties<br>
<br>
4.5. Databankspecificaties en beheer van de GRB-databank<br>
<br>
5. De uitwisseling van gegevens met het GRB<br>
<br>
5.1. Algemeen<br>
<br>
5.2. Productspecificaties<br>
<br>
5.2.1. productstructuur<br>
<br>
5.2.2. update-versies<br>
<br>
5.3. Bijhoudingsspecificaties<br>
<br>
5.3.1. meldingsprocedure<br>
<br>
5.3.2. opdrachtdefiniëring<br>
<br>
5.3.3. data-inwinning<br>
<br>
5.3.4. grafische integratie<br>
<br>
5.3.5. integratie van gegevens in GRB-beheersdatabank<br>
<br>
5.3.6. productverspreiding<br>
<br>
5.4. Uitwisseling met andere databronnen<br>
<br>
6. Lexicon<br>
<br>
1. INLEIDING<br>
<br>
Deze bijlage omvat de minimum technische bepalingen inzake<br>
<br>
• Het opmeten van grootschalige gegevens.<br>
<br>
• De opname van grootschalige geografische gegevens in het GRB.<br>
<br>
• De uitwisseling van gegevens met het GRB.<br>
<br>
Een eerste hoofdstuk is gewijd aan specifieke GRB-terminologie en definities.<br>
<br>
2. GRB-TERMINOLOGIE<br>
<br>
In tegenstelling tot de kaartgerichte initiatieven volgt het GRB een objectgerichte databank benadering.<br>
<br>
2.1. Objectgerichtheid<br>
<br>
De term objectgericht slaat in deze context op de aanwezigheid van gegevens die rechtstreeks verwijzen naar terreinobjecten (zie figuur 1).<br>
<br>
Een object is een onafhankelijk en herkenbaar fenomeen van de werkelijkheid dat kan gelokaliseerd worden op het aardoppervlak. De beschrijvende waarneembare elementen van een object worden eigenschappen genoemd. De wezenlijke karakteristieke eigenschappen van een dergelijk object heten kenmerken. In het dagelijkse leven worden de kenmerken van de objecten aangegrepen om de veelheid van fenomenen te typeren en groeperen volgens min of meer conventionele definities. Objecten kunnen tot een zelfde definitie behoren, maar toch bepaalde afwijkende kenmerken bezitten. Een deel van een verzameling objecten waarvan minstens één<br>
<br>
kenmerk niet in de definitie van het object is opgenomen, kunnen in de databank aanleiding geven tot het ontstaan van verschillende types.<br>
<br>
De databank ordent de objecten volgens databankentiteiten. Dit zijn abstracties van objecten met gelijkaardige eigenschappen. De kenmerken en eigenschappen van de objecten worden naargelang de entiteit gemodeleerd in attributen, met een domein of bereik voor bijbehorende waarden. Een databankexemplaar omvat de voorkomende gegevens van een opgenomen object met een waarde voor elk attribuut. Bepaalde attributen zullen een verdere typering van de entiteit mogelijk maken, uitgaande van afwijkende kenmerken die niet in de definitie zijn opgenomen.<br>
<br>
Een verband dat entiteiten samenbrengt volgens structurele relaties, noemt men conventioneel een thema. In beginsel gaat het om verbanden die een nevenschikkend of een beschrijvend karakter bezitten, zo zijn er bijvoorbeeld zowel wegknopen als tussenliggende wegverbindingen nodig om een operationeel wegnetwerk op te bouwen. Het thema schept een afgelijnd ontwikkelingskader dat toelaat de specificaties van de samengevoegde entiteiten fijner op elkaar af te stemmen. De entiteiten behouden evenwel hun zelfstandigheid bij inwinning, bijhouding en gebruik.<br>
<br>
Uit de objectgerichte databank is een product op de klassieke laaggerichte manier, bedoeld voor de CAD-systemen af te leiden. Een zogenaamde DXF-layer bevat gegevens van één of meerdere databankexemplaren terwijl gegevens van een databankexemplaar kunnen opgeslagen worden op verschillende DXF-layers.<br>
<br>
figuur 1: niet opgenomen<br>
<br>
2.2. Identificatoren<br>
<br>
De herkenbaarheid van het terreinobject impliceert dat het exemplaar in de databank er éénduidig mee in verband kan gebracht worden. Daarom is het gebruik van een unieke identificator per exemplaar noodzakelijk. Hierbij worden de volgende regels gerespecteerd :<br>
<br>
• de identificator is per definitie een volgnummer zonder betekenis of functie (een sleutel volgens de relationele theorie);<br>
<br>
• de nummering geschiedt onafhankelijk per entiteit (of laag);<br>
<br>
• er is slechts één instantie bevoegd voor de definitieve toekenning van identificatoren.<br>
<br>
Objectidentificatie in GRB gebeurt aan de hand van 2 ID's : een objectID en een unieke ID.<br>
<br>
De objectID (oidn) is de directe link naar een terreinobject. De waarde voor de ID blijft steeds dezelfde.<br>
<br>
De unieke ID (uidn) is de directe link naar de « verschijningstoestand » van een terreinobject. Een terreinobject kan inderdaad veranderen van vorm of van eigenschappen. Wanneer deze wijziging ook in de databank wordt aangebracht, dan krijgt de record een nieuwe uidn.<br>
<br>
Een identificator kan slechts één enkele maal gebruikt worden. Verdwijnt een terreinobject, dan verdwijnt het overeenkomstig exemplaar en wordt de bijbehorende identificator passief gemaakt. Dit passieve gegeven wordt als archief en voor historische reconstructie bewaard. Aan een nieuw databank exemplaar wordt steeds een nooit eerder gebruikte identificator toegekend.<br>
<br>
2.3. GRB-specificaties<br>
<br>
Er zijn een aantal specificaties ontwikkeld die aan een specifiek doel of gebruik tegemotkomen.<br>
<br>
Volgende sets specificaties zijn vastgelegd :<br>
<br>
• De aanmaakspecificaties : een specificatie in bestekvorm die gebruikt wordt om de aanmaak van GRB door externe aannemers mogelijk te maken.<br>
<br>
• De databankspecificaties : een specificatie die de gegevens van het GRB beschrijft in het databanksysteem, bedoeld voor het beheer en de processen van bijhouding van de GRB-gegevens.<br>
<br>
• De procutspecificaties : specificaties die de technische kenmerken van de GRB-producten beschrijven ten behoeve van de gebruikers.<br>
<br>
• De skeletspecificaties : een specificatie voor GRB-compatibele terrestrische opmetingen.<br>
<br>
• De bijhoudingsspecificaties : specificaties die moeten toelaten dat de gebruikers actief gegevens kunnen aanleveren in het kader van de GRB-bijhouding. De opmeting van de nieuwe data gebeurt op basis van de skeletspecificaties, variant bijhouding.<br>
<br>
• De kwaliteitsspecificaties : het geheel van afspraken en normen omtrent de uitvoering van kwaliteitscontroles op de GRB-gegevens.<br>
<br>
3. HET OPMETEN VAN GROOTSCHALIGE GEOGRAFISCHE GEGEVENS<br>
<br>
3.1. FLEPOS<br>
<br>
FLEPOS staat voor FLEmish POsition Service, een op satellietnavigatie-gebaseerd plaatsbepalingsysteem met centimeter nauwkeurigheid.<br>
<br>
FLEPOS biedt als operationeel systeem voor uniforme en nauwkeurige plaatsbepaling de vereiste stabiliteit die nodig is om diverse metingen uit talrijke bronnen met elkaar te integreren, vandaar dat zij als grondslag wordt opgelegd voor de bepaling van de geografische coördinaten bij de GRB-specificaties (cfr. Art. 7). De opmeting van de data gebeurt in het Lambert-BD72/50 systeem en de hoogtes worden geregistreerd t.o.v. TAW.<br>
<br>
3.2. Data-inwinning<br>
<br>
3.2.1. aanmaakspecificaties<br>
<br>
De aanmaakspecificaties worden opgemaakt t.b.v. de bestekken voor de aannemers. De aannemer dient de data volgens deze aanmaakspecificaties aan het Agentschap voor Geografische Informatie Vlaanderen te bezorgen. Hierbij wendt hij een aantal technieken aan.<br>
<br>
Allereerst wordt van de betrokken projectzone een fotovlucht gerealiseerd. Deze grootschalige luchtopnames worden gebruikt voor de aanmaak van orthofoto's en de fotorestitutie. Aanvullend worden gegevens ingewonnen m.b.v. terrestrische technieken op het terrein. Eventueel dient de aannemer rekening te houden met recuperatie<br>
<br>
van bestaand materiaal. Tenslotte dient hij via de methode van de herinterpretatie administratieve percelen op te bouwen.<br>
<br>
3.2.2. aanmaaktechnieken<br>
<br>
3.2.2.1. fotogrammetrie<br>
<br>
luchtfoto's<br>
<br>
De luchtfoto's worden genomen met een metrische camera op een fotoschaal die aan de vereisten van een grootschalige kartering beantwoordt. Na keuring worden deze luchtfoto's verwerkt tot digitale rasterbestanden met een minimale grondresolutie van 8 cm, RGB (24 bit).<br>
<br>
orthofoto's<br>
<br>
Voor aanmaak van orthofoto's en de verdere verwerking van de fotorestitutie wordt een aerotriangulatie en blokvereffening uitgevoerd. Daarnaast wordt een digitaal hoogtemodel gebruikt met een minimum grid van 50 x 50 meter voor de opbouw van de orthofoto.<br>
<br>
Deze orthofoto's worden aangewend voor de controle van de gegevens en voor de aanmaak van de administratieve percelen.<br>
<br>
fotorestitutie<br>
<br>
Op basis van fotorestitutie worden de entiteiten in een 3-D zicht geïnventariseerd. De fotorestitutie biedt het voordeel de achterliggende gevels in afgesloten huizenblokken vlot te digitaliseren, daar waar een terrestrische, topografische meting niet evident is.<br>
<br>
3.2.2.2. terrestrische opmetingen<br>
<br>
Op het terrein dienen nog een aantal entiteiten aangevuld, gecorrigeerd of nieuw opgemeten.<br>
<br>
Entiteiten die een hoge procisie vragen worden op het terrein met behulp van tachymetrische instrumenten en GPS-ontvangers opgemeten. Een bijzondere vorm van terrestrische opmeting betreft het skeletbestek, dat aangewend kan worden voor ad-hoc metingen. De kernbepalingen van het skeletbestek zijn opgesteld dat een<br>
<br>
maximale recupereerbaarheid in het GRB kan worden gerealiseerd. Ze vormen tevens de basis voor de bijhoudingsmetingen voor het GRB. Voor entiteiten die een lagere precisie vragen, kunnen ook andere meettechnieken volstaan.<br>
<br>
3.2.2.3. recuperatie<br>
<br>
Indien er bestaand materiaal aanwezig is en dat voldot aan de kwaliteitsspecificaties van het GRB, kan dit geheel of gedeeltelijk gerecupereerd worden in het GRB. De aannemer dient deze gegevens, waar die nog actueel zijn, te integreren in het GRB.<br>
<br>
3.2.2.4. methodiek herinterpretatie percelen<br>
<br>
Op basis van de orthofoto's, de reeds gekarteerde exemplaren van het GRB en de KADSCAN/KADVEC bestanden, wordt een herinterpretatie uitgevoerd van de kadastrale percelen tot administratieve percelen. Het administratief perceel is een grafische voostelling van de vermoedelijke ligging van het kadastraal perceel, waarbij de perceelsgrenzen werden geïnterpreteerd rekening houdend met de terreinsituatie.<br>
<br>
3.2.3. GRB-skeletbestekken<br>
<br>
De GRB-skeletbestekken vormen een set van gestandaardiseerde technische bepalingen met het oog op de oplevering van GRB-compatibele gegevens via gangbare teerestrische opmetingen in gebieden waar geen GRB-producten beschikbaar zijn. Er bestaan verschillende varianten van het GRB-skeletbestek rekening houdende<br>
<br>
met sectoriële « aanvullingen » en toepassingspecifieke « opties ». De modulaire aanpak bevordert het verwijzen naar gemeenschappelijke sets van GRB-speficiaties onder de vorm van kant en klare bestekken.<br>
<br>
De gemeenschappelijke basis van elk van deze GRB-skeletvarianten wordt gevormd door de zogenaamde « kernbepalingen ».<br>
<br>
De gegevens volgend uit de kernbepalingen bestaan onder de vorm van DXF-bestanden en zijn uitsluitend referentiegegevens die in aanmerking komen voor recuperatie bij de GRB-projectkarteringen. De kernbepalingen vormen tevens de basis voor de GRB-skeletmetingen ten behoeve van de bijhouding.<br>
<br>
4. DE OPNAME VAN GROOTSCHALIGE GEOGRAFISCHE GEGEVENS IN HET GRB<br>
<br>
4.1. Referentiegegevens<br>
<br>
In eerste instantie is het GRB een grootschalige kartering. Terreingegevens worden met een precisie ingewonnen die een normaal gebruik toelaten in het schaalbereik 1/250 - 1/2500.<br>
<br>
Het gebruik van de term grootschalig referentiebestaand duidt aan dat de opgenomen gegevens als referentie dienen voor bijkomende thematische gegevens. Als criterium voor opname in het hierna voorgestelde GRB-model worden enkele eenvoudige vuistregels gehanteerd. Een gegeven wordt weerhouden indien :<br>
<br>
• het mogelijk is een volledige en ondubbelzinnige specificatie op te maken;<br>
<br>
• de opgenomen informatie aangesproken wordt door verscheidene gebruikers;<br>
<br>
• verschillende processen of applicaties de opgeslagen gegevens verwerken;<br>
<br>
• de informatie noodzakelijk is voor de uitbouw van andere, externe gegevensbanken.<br>
<br>
De entiteit « gebouw » illustreert op duidelijke wijze het voorkomen van een harde definitie van meerdere gebruikers (nutsbedrijven en administraties), van meerdere toepassingsmogelijkheden (leidingregistratie en vergunningenbeleid) evenals mogelijke koppelingen naar een extern gegevensbestand (bewoners).<br>
<br>
Indien een gegeven niet aan de vuistregels beantwoordt, dan wordt het in beginsel niet als referentiegegeven weerhouden.<br>
<br>
Tenslotte worden de gegevens beheerd als een bestand en niet langer als een snel verouderende kaart. De belangrijkste voordelen ten opzichte van een puur cartografische benadering zijn de beheersbaarheid van een grote hoeveelheid geografische informatie, de integratie van de gegevens in een GIS-omgeving, de reproduceerbaarheid in verschillende vormen en het inzetten van uitgebreide controletools voor de kwaliteitsbeheersing. Daarenboven biedt ene databankomgeving meer mogelijkheden voor een gecontroleerde bijhouding.<br>
<br>
4.2. GRB-entiteiten volgens de GRB-terreinclassificatie<br>
<br>
Bij de inventarisatie wordt het terrein beschouwd als een verzameling van onafhankelijke fenomenen (« objecten ») die volgens entiteiten worden gegroepeerd. Voor elke entiteit is een beschrijvende fiche met o.a. de definitie, de types, selectiecriteria, voorwaarden, kwaliteitsacpecten en attributen. Entiteiten worden gegroepeerd tot<br>
<br>
een thema. Enkel die terreingegevens die duidelijk te specificeren zijn en waarvoor de referentiewaarde ontegensprekelijk vaststaat, worden opgenomen in de databank.<br>
<br>
De GRB-producten bevatten gegevens afgeleid uit de GRB-databank, de zogenaamde productentiteiten. Deze productentiteiten zijn te onderscheiden via de naamgeving van de bestanden. Er wordt hierbij gebruik gemaakt van handige en goed herkenbare acroniemen.<br>
<br>
4.3. Overzicht thema's en entiteiten van GRB<br>
&nbsp;</p>

<table border="1" cellpadding="0" cellspacing="0" style="border-collapse:collapse">
	<tbody>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:windowtext 1pt solid; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Thema<!--?xml:namespace         prefix = o ns = "urn:schemas-microsoft-com:office:office"         /--></p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:windowtext 1pt solid; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>Entiteit</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:windowtext 1pt solid; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>Beschrijving</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:windowtext 1pt solid; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>Type</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Mkr - meetkundige referentie</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>mkp</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>planimetrisch geodetisch punt</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>&nbsp;</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>mkv</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>GPS-verdichtingspunt</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td rowspan="7" style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Inr - inrichtingselementen</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>gbg</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>gebouw aan de grond</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:149.2pt">
			<p>1: hoofdgebouw</p>

			<p>2: bijgebouw</p>

			<p>3: gebouw afgezoomd met virtuele gevels</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>adr</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>deelcomponent adres</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>gvl</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>gevellijn van een gebouw</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: terrestrisch gemeten gevellijn</p>

			<p>2: fotogrammetrische gevellijn (dakoversteek met terugzetting)</p>

			<p>3: fotogrammetrische gevellijn (dakrand)</p>

			<p>4: fotogrammetrische gevellijn (dakoversteek)</p>

			<p>5: gerecupereerde gevellijn uit bestaand kaartmateriaal</p>

			<p>6: geconstrueerde gevellijn</p>

			<p>7: niet-duurzame gemene gevellijn</p>

			<p>8: kadastrale gevellijn</p>

			<p>9: fictieve gevellijn</p>

			<p>10: gedeeltelijke terrestrisch gemeten gevellijn (gevelstuk)</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>gvp</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>gevelpunt van een gebouw</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: terrestrisch gemeten gevelpunt</p>

			<p>2: fotogrammetrisch gevelpunt (dakoversteek met terugzetting)</p>

			<p>3: fotogrammetrisch gevelpunt (dakrand)</p>

			<p>4: fotogrammetrisch gevelpunt (dakoversteek)</p>

			<p>5: gerecupereerd gevelpunt uit bestaand kaartmateriaal</p>

			<p>6: geconstrueerd gevelpunt</p>

			<p>7: niet-duurzame gemeen gevelpunt</p>

			<p>8: kadastrale gevelpunt</p>

			<p>9: fictieve gevelpunt</p>

			<p>10: gevelstukpunt</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>gba</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>gebouwaanhorigheid</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: verdieping</p>

			<p>2: afdak</p>

			<p>3: loopbrug</p>

			<p>4: trap</p>

			<p>5: zichtbare onderkeldering</p>

			<p>6: ingezonken geragetoegang</p>

			<p>7: uitbreiding</p>

			<p>10: dakoversteek</p>

			<p>11: verheven garagetoegang</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>knw</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>kunstwerk</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: overbrugging</p>

			<p>2: waterbouwkundige constructie</p>

			<p>3: cultuur-historisch monument</p>

			<p>4: hoogspanningsmast/openbare TV-mast</p>

			<p>5: pijler</p>

			<p>6: rooster</p>

			<p>7: schoorsteen</p>

			<p>8: koeltoren</p>

			<p>9: silo, opslagtank</p>

			<p>10: cabine</p>

			<p>11: watertoren</p>

			<p>12: tunnelmond</p>

			<p>13: chemische installatie</p>

			<p>22: golfbreker</p>

			<p>23: havenpier</p>

			<p>24: staketsel</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wga</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>wegaanhorigheid</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: bushok</p>

			<p>2: telefooncabine</p>

			<p>3: overdekte fietsstalling</p>

			<p>5: bergplaats</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Wbn - wegbaan</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wbn</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>wegbaan</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:149.2pt">
			<p>1: kruispuntzone</p>

			<p>2: wegsegment</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:119.05pt">
			<p>Trn - terrein</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>trn</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>terrein</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:119.05pt">
			<p>Sbn - spoorbaan</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>sbn</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>spoorbaan</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Wgo - wegopdeling</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wgo</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>wegopdeling</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: grens circulatiezone zwakke weggebruiker (wcz)</p>

			<p>2: grens onverharde zone (woz)</p>

			<p>3 : rand van de rijbaan (wrb)</p>
			</td>
		</tr>
		<tr>
			<td rowspan="4" style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Wgi - weginrichting</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wpi</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>puntvormige weginrichting</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: paal</p>

			<p>2: meerpaal</p>

			<p>4: brandkraan</p>

			<p>5: grenspaal</p>

			<p>6: paal waarop een publieke telefoon is gemonteerd, praatpaal</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wli</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>longitudinale weginrichting</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: verhoogde boord- of kantsteen</p>

			<p>2: muur, stootband</p>

			<p>3: vangrail</p>

			<p>9: niet-afgeboorde verhoging</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wti</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>transversale weginrichting</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:149.2pt">
			<p>1: verhoogde drempel</p>

			<p>2: verlaging</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wrl</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>spoorrail</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td rowspan="4" style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Wtr - oppervlaktewater</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>wtz</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>watergangzone</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wgl</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>rand van watergang</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: reële grenslijn</p>

			<p>2: benaderde grenslijn</p>

			<p>3: virtuele grenslijn</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>wgr</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>gracht</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>wri</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>zichtbaar putdeksel</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:149.2pt">
			<p>1: crikelvorming putdeksel</p>

			<p>2: vierkant putdeksel</p>
			</td>
		</tr>
		<tr>
			<td rowspan="2" style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Kad - kadastrale indeling</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>adp</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>adp administratieve percelen</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>prp</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>zichtbare grenspaal</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td rowspan="2" style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Grb - grb-ondersteunende entiteiten</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:65.2pt">
			<p>inv</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:127.6pt">
			<p>zone van inventarisatieopdracht</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>1: GRB initiële kartering</p>

			<p>2: GRB-skeletmeting</p>

			<p>3: GRB-bijhoudingsproject</p>

			<p>4: GRB-skeletmeting in het kader van de bijhouding</p>

			<p>5: CARDIB-kartering</p>

			<p>6: Netmanagement-kartering</p>

			<p>7: Interelectra-kartering</p>

			<p>8: HAVI-kartering</p>

			<p>9: Alfanumerieke inventarisatie</p>

			<p>10: adp-opdracht</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>ano</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>zone van anomalie</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td rowspan="2" style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Wegennetwerk</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>wvb</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>wegverbinding</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>wkn</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>wegknoop</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td rowspan="2" style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:windowtext 1pt solid; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:119.05pt">
			<p>Waterwegennetwerk VHA</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>vhag</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>vha-gewestcode</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:65.2pt">
			<p>vhas</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; width:127.6pt">
			<p>vha-segmentcode</p>
			</td>
			<td style="background-color:transparent; border-bottom:windowtext 1pt solid; border-left:#f0f0f0; border-right:windowtext 1pt solid; border-top:#f0f0f0; height:11.35pt; vertical-align:top; width:149.2pt">
			<p>&nbsp;</p>
			</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>

<p>&nbsp;</p>

<p>4.4. Kwaliteitspecificaties<br>
<br>
De kwaliteit van gegevens is sterk bepalend voor het gewenste gebruik, vooral in relatie met themalagen die zelf door een eigen kwaliteit gekenmerkt worden. Kwaliteit wordt beschreven door alle kenmerken en eigenschappen van de verzamelde gegevens die bijdragen tot het vermogen te voldoen aan uitdrukkelijke of impliciete noden. De kwaliteit wordt dus vooral benaderd vanuit de gebruiksverwachtingen. Zo wordt bijvoorbeeld een gebeidsdekkende inventaris verwacht van het GRB die bovendien direct bruikbaar is binnen een geografisch informatie systeem (GIS). Dit vraagt specifieke aandacht naar volledigheid enerzijds en digitale en grafische<br>
<br>
consistentie anderzijds. De behoeft naar de volledigheid van GRB- gegevens varieert afhankelijk van de interessegebieden van de gebruikers. Zo worden gegevens in het binnengebied doorgaans minder streng gecontroleerd dan gegevens met betrekking tot het openbaar domein. Dit komt overeen met de verwachtingen van de gebruikers.<br>
<br>
Ook de positionele precisie is functie van kwaliteit. Zo willen landmeters gebruik maken van zeer precieze GRB-grondslaggegevens voor de aansluiting van bijhoudingsmetingen terwijl de tekenkamers van de nutsbedrijven een zekere precisie vragen met het oog op het gebruik van GRB-gegevens voor leidingregistratie.<br>
<br>
De kwaliteit wordt in het geval van de GRB-gegevens gemeten aan de hand van de kwaliteitsindicator AQL. Dit is het percentage fouten in GRB dat omzeggens steeds zal aanvaard worden tijdens controle. Het is immers onmogelijk om in deze context een foutloos bestand te eisen van de uitvoerder. Fouten die in de databank gekend<br>
<br>
zijn worden in het product aangegeven via de afgeleide entiteit anomalie (ano).<br>
<br>
De AQL-waarden (en dus de kwaliteit van de GRB-gegevens) variëren in functie van :<br>
<br>
• de verwachtingen en interessegebied van gebruikers;<br>
<br>
• de specificaties van entiteiten : waar worden moeilijkheden verwacht ?;<br>
<br>
• de karteringstechniek die gebruik werd voor de inwinning;<br>
<br>
• de kostprijs om de kwaliteit van de gegevens ter verzekeren;<br>
<br>
• de precisie waarmee het object in het terrein aan te meten is, onafhankelijk van de gebruikte karteringstechniek.<br>
<br>
In een karteringsproject kan de uitvoerder gebruik maken van drie karterings-technieken :<br>
<br>
• terrestrische metingen;<br>
<br>
• restitutie via luchtfotogrammetrie;<br>
<br>
• conversie van bestaand grootschalig kaartmateriaal.<br>
<br>
Dit betekend dat de positionele precisie van GRB-gegevens als volgt kan beschreven worden :<br>
<br>
• terrestrische metingen leveren doorgaans de meest precieze resultaten op. Deze gegevens worden gebruikt om bijhoudingsmetingen aan te sluien aan Lambert BD72/50. Er wordt gemiddeld slechts 2,5 % overschrijdingen boven 15 cm toegestaan binnen een stukje GRB;<br>
<br>
• de inspanningen die gebeuren via luchtfotogrammetrie zijn minder precies. Doorgaans worden deze gebruikt in functie van :<br>
<br>
• leidingregistratie : er wordt gemiddeld slechts 2,5 % overschrijdingen boven 30 cm toegestaan;<br>
<br>
• cartografische visualisatie : er wordt gemiddeld slechts 2,5 % overschrijdingen boven 50 cm toegestaan.<br>
<br>
De drempelwaarden die hierboven vermeld worden zijn van toepassing op een puntsgewijze evaluatie binnen een steekproef. De kwaliteitsindicator voor het volledige punten- of lijnenveld is vanzelfsprekend strenger en kan hiervan afgeleid worden.<br>
<br>
Bij de aanmaak van de GRB-data refereert de actualiteit naar de leveringsdatum van de deellevering door de aannemer. Voor de percelen verwijst die naar de kadastrale toestand van de op dat moment beschikbare KADSCAN-KADVEC bestanden.<br>
<br>
Fouten die in de databank gekend maar nog niet verbeterd zijn worden in het product aangegeven via de afgeleide entiteit anomalie (ano). Deze entiteit wordt algemeen genomen gebruikt voor het aankondigen van veranderingen in de GRB-gegevens, bijvoorbeeld naar aanleiding van terreinmutaties (heraanleg van een weg, nieuw gebouw, ...) en/of vastgestelde fouten tijdens de kwaliteitscontrole.<br>
<br>
4.5. Databankspecificaties en beheer van de GRB-databank<br>
<br>
De databankspecificaties regelen de opname en het beheer van de GRB-gegevens in de databank.<br>
<br>
Bij invoeren van de data in de GRB-databank worden nog een aantal extra controles uitgevoerd naar topologische regels (bv. aansluiting tussen 2 GRB-projectzones, ...), consistentieregels tussen de verschillende entiteiten, opbouw historiek en toekenning unieke identificatoren. Aan ieder exemplaar wordt volgens de<br>
<br>
databankspecificaties een objectidentificator (oidn) en een unieke identificator (uidn) toegekend. Ieder exemplaar in de databank heeft een levensloop (ontstaan, eventueel wijzigen, verdwijnen). Op deze manier kan historiek in de databank opgebouwd worden en deze vormen ook de basis voor de bijhouding.<br>
<br>
De anomalieën, dit zijn geverifieerde GRB-afwijkingen, worden eveneens in de databank beheerd en opgevolgd.<br>
<br>
5. DE UITWISSELING VAN GEGEVENS MET HET GRB<br>
<br>
5.1. Algemeen<br>
<br>
Eenmaal de gegevens van de aannemers goedgekeurd zijn, worden de GRB-data in de GRB-databank gebracht. Er worden unieke udentificatoren toegekend. De uitwisseling met de GRB-databank start bij de aanmaak van een product van het GRB. Dit product kan ofwel een databank ofwel een klassieke kaartvoorstelling inhouden. Op basis van dit product zal een communicatie ontstaan met de GRB-databank, onder vorm van melding van wijzigingen. De bijhouding vormt de belangrijkste wisselwerking van data met het GRB.<br>
<br>
Het GRB biedt een aantal sleutels aan (perceelsidentificatie, adres, wegregistratie, ...) waardoor een koppeling mogelijk gemaakt wordt met andere externe databronnen. Zo levert het GRB de geografische referentie aan voor thematische gegevens. Een Ruimtelijk Uitvoeringsplan (RUP) kan gebaseerd zijn op de geografische referentie van het GRB. Dit wordt schematisch voorgesteld in onderstaande figuur :<br>
<br>
Figuur 2 : GRB-uitwisseling (niet opgenomen)<br>
<br>
Centraal staat de GRB-databank met zijn referentiegegevens. Koppeling via sleutelvelden is mogelijk met andere informatiesystemen (bv. het adres). Het GRB-kader omvat het breder draagvlak van het GRB, met de omschrijving van het decretaal kader, de organisatie van het GRB, de ondersteuning en modelijke toepassingen van GRB, de methodiek van gegevensuitwisseling en in het bijzonder de bijhouding.<br>
<br>
5.2. Productspecificaties<br>
<br>
5.2.1. productstructuur<br>
<br>
De GRB-gegevens worden naar inhoud in entiteiten of geografische lagen ingedeeld. Voorbeelden van entiteiten zijn gbg (gebouw aan de grond) en wbn (wegbaan). De gegevens met betrekking tot deze entiteiten kunnen in verschillende producten van het Agentschap voor Geografische Informatie Vlaanderen opgenomen worden. Een aantal entiteiten in GRB worden afgestemd op basis van andere beheersdatabanken (VHA, CRAB, A.A.P.D.) en verzekeren de comptabiliteit met de entiteiten uit deze beheersdatabanken. Zo bestaat het waterlopennetwerk in GRB uit een extract van de VHA. Waar dit relevant is wordt adresinformatie uit het CRAB in de producten opgenomen. Zo bevat de entiteit gbg (gebouw aand e grond) straatnaam- en huisnummergegevens; de entiteit wvb (wegverbinding) bevat straatnaaminformatie. De administratieve percelen (adp) verwijzen via de perceelsidentificatie naar de kadastrale percelen, beheer door de A.A.P.D.<br>
<br>
Met betrekking tot het GRB worden producten aangemaakt volgens 2 verschillence types formaten : enerzijds als een set van GIS-bestanden, anderzijds als een digitale kaart. De GIS-bestanden stellen de individuele GIS-gebruikers in staat om de referentiegegevens te integreren in hun eigen GIS-omgeving. Ze kunnen zonderproblemen gecombineerd worden met gebruikerseigen thematische bestanden.<br>
<br>
De digitale kaart van het GRB is gestructureerd in verschillende DXF-lagen. Dit product is in eerste instantie bedoeld voor ontwerpers en tekenaars in alle segmenten van AM/FM. Daarnaast vormt dit product tevens een belangrijke schakel in het GRB-bijhoudingsproces.<br>
<br>
In deze digitale kaart zijn de gegevens verwerkt van alle GRB-entiteiten zoals vermeld in tabel 1. Straatnaam- en huisnummergegevens uit het CRAB en de naam van waterlopen uit het VHA-product zijn als tekst geïntegreerd.<br>
<br>
De opname van de GRB-gegevens in zogenaamde GRB-karteringsprojecten gebeurt hoofdzakelijk in 2D. Nochtans zijn er reeds lange tijd mogelijkheden voor het aanleveren van 3D-informatie, zowel via terrestrische metingen als via fotogrammatrische methodes. Het Agentschap voor Geografische Informatie Vlaanderen heeft ervoor geopteerd in het<br>
<br>
GRB-model enkel hoogtegegevens op te slaan voor volgende entiteiten :<br>
<br>
• meetkundig verdichtingspunt van het planimetrisch geodetisch (mkp);<br>
<br>
• meetkundig verdichtingspunt (mkv);<br>
<br>
• putdeksels (wri).<br>
<br>
Alle overige entiteiten hebben enkel een x,y-coördinaat binnen Lambert BD72/50.<br>
<br>
5.2.2. update-versies<br>
<br>
5.2.2.1. delta-versies<br>
<br>
Delta-versies leveren de verschillen aan t.o.v. de vorige versie van de GIS-bestanden van GRB. Het voordeel is dat ze beperkt in omvang en vrij snel aan te leveren zijn.<br>
<br>
5.2.2.2. complete dataset updates (per jaar)<br>
<br>
Minimaal 1 maal per jaar zal een nieuwe versie uitgebracht worden met de bijgewerkte GRB-data; dit is steeds het startbestand om verder met delta versies te werken.<br>
<br>
In principe zal het digitale kaart product steeds een volledig nieuwe datset inhouden.<br>
<br>
5.3. Bijhoudingsspecificaties<br>
<br>
De bijhouding is een organisatie-overschrijdend proces waarbij oa. gegevensuitwisseling plaatsvindt. Er bestaan specificaties voor melding, opdrachtdefiniëring, data-inwinning, data-verwerking, kwaliteitscontrole, gegevensuitwisseling en distributie.<br>
<br>
5.3.1. meldingsprocedure<br>
<br>
Een afwijking definiëren we als elke situatie waarbij het GRB niet overeenkomt met de terreinsituatie. Dit kan zowel een terreinmutatie als een fout/onvolledigheid van de bestaande GRB-data inhouden. De melding van een afwijking wordt op een gestructureerde manier aan het Agentschap voor Geografische Informatie Vlaanderen overgemaakt. Zoals in het GRB-decreet, art. 13 gestipuleerd dienen gebruikers van het GRB afwijkingen te melden aan het Agentschap voor Geografische Informatie Vlaanderen.<br>
<br>
Het Agentschap voor Geografische Informatie Vlaanderen controleert de afwijking en de anomalie wordt in de databank opgenomen, todat er een nieuwe gegevens voor die afwijking beschikbaar komen.<br>
<br>
5.3.2. opdrachtdefiniëring<br>
<br>
Het definiëren van terrestrische meetopdrachten in het scenario van bijhouding steunt op een aantal richtlijnen omtrent de aan te leveren basisgegevens (het zogenaamde « GRB-extract ») en de ruimtelijke en inhoudelijke beschrijving van de karteringsopdracht. Ook de verwijzing naar de relevante GRB-skeletspecificaties wordt in deze fase verzorgd.<br>
<br>
5.3.3. data-inwinning<br>
<br>
In de meeste gevallen zal de inwinning gebeuren aan de hand van terrestrische metingen. Hiervoor wordt gebruik gemaakt van de GRB-skeletvariant bijhouding als set van minimale bepalingen voor de oplevering van GRB-compatibele gegevens. Doorgaans zullen deze specificaties toegepast worden op as-built plannen, bijvoorbeeld<br>
<br>
horende bij een wegenisdossier. De kwaliteitsspecificaties die deel uitmaken van de GRB-skeletvariante bijhouding zorgen ervoor dat de recuperatie van de aangeboden gegevens de kwaliteit van de GRB-databank niet doet afnemen na verloop van tijd.<br>
<br>
Voor andere afwijkingen is de recuperatie van bestaande karteringsprocessen niet mogelijk. De specificaties voor data-uitwisseling met externe databanken van diverse partners zorgen ervoor dat de bijhouding in de private ruimte zo goed als mogelijk wordt uitgevoerd. Waar nodig zal getracht worden de overige anomalieën<br>
<br>
weg te werken via gerichte bijhoudingsprojecten.<br>
<br>
5.3.4. grafische integratie<br>
<br>
Vooraleer een unieke en éénduidige geometrie kan aangeboden worden, dient een grafische integratie uitgevoerd te worden. Hiertoe worden een aantal principes en richtlijnen gehanteerd zodat de kwaliteit van de oplossing niet wordt aangetast.<br>
<br>
5.3.5. integratie van gegevens in GRB-beheersdatabank<br>
<br>
De goedgekeurde leveringen in het kader van de bijhouding worden ingelezen in de databank. Hierbij vindt de objectvorming plaats waarbij het historiekmodel van de databank de wijziging van de objectidentificatoren regelt en de verdwenen of gewijzigde exemplaren opslaat.<br>
<br>
De anomaliemelding wordt eveneens als historisch gegeven opgeslagen.<br>
<br>
5.3.6. productverspreiding<br>
<br>
De nieuwe, geactualiseerde data komen terug ter beschikking onder vorm van de hierboven beschreven productspecificaties.<br>
<br>
5.4. Uitwisseling met andere databronnen<br>
<br>
De uitwisseling en terugkoppeling met andere databronnen levert extra controles en mogelijkheden om afwijkingen te detecteren en mogelijk te corrigeren.<br>
<br>
Zo kan de koppeling via de perceelsinformatie met de kadastrale legger aanduiding geven waar zich wijzigingen op het private domein hebben voorgedaan of kan de koppelingen met het plannen- en vergunningenregister indicaties geven waar in de toekomst mutaties zullen gebeuren.<br>
<br>
6. LEXICON<br>
<br>
2-D : twee dimensioneel<br>
<br>
3-D : drie dimensioneel<br>
<br>
A.A.P.D. : FOD Financiën, Algemene Administratie van de Patrimoniumdocumentatie<br>
<br>
AM/FM : Automated mapping/Facility Management<br>
<br>
AQL : Acceptable Quality level<br>
<br>
BD72/50 : Belgian Datum 72/50<br>
<br>
CAD-systemen : Computer Aided Drafting systemen<br>
<br>
CRAB : Centraal Referentie Adressen Bestand<br>
<br>
DXF : Drawing eXchange format<br>
<br>
GIS : Geografisch Informatie Systeem<br>
<br>
GPS : Global Positioning System<br>
<br>
GRB : Grootschalig Referentie Bestand<br>
<br>
ID : identifier<br>
<br>
FLEPOS : Flemish Positioning Service<br>
<br>
KADSCAN : gescande, gegeorefereerde kopie van de kadastrale perceelsplans met perceelsindentificatie<br>
<br>
KADVEC : plangetrouwe vectorisering van de KADSCAN-bestaan<br>
<br>
RGB : Red-Green-Blue<br>
<br>
RUP : Ruimtelijk Uitvoeringsplan<br>
<br>
TAW : Tweede Algemen Waterpassing<br>
<br>
VHA : Vlaams Hydrografische Atlas</p>
