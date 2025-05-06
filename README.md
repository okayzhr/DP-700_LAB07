# DP-700_LAB07
# 📊 Microsoft Fabric Real-Time Data Project

Beschrijving:
Dit project laat zien hoe je met Microsoft Fabric real-time gegevens van een beursvoorbeeld kunt streamen, opslaan, analyseren en visualiseren. Het doel is om een volledig data-analyseproces op te zetten met behulp van Eventstream, Eventhouse, KQL-query's, dashboards en waarschuwingen via Activator.

Stappen:

1. Werkruimte aanmaken:
   - Ga naar https://app.fabric.microsoft.com.
   - Maak een nieuwe werkruimte aan met Fabric-capaciteit ingeschakeld (Trial, Premium of Fabric).
   - De werkruimte is nu klaar om gegevens te ontvangen.

2. Eventstream maken:
   - Navigeer naar de Real-Time hub.
   - Verbind met de voorbeeldgegevensbron "Stock market".
   - Geef de eventstream de naam: stock-data.
   - Open de eventstream en bekijk de stroom.

3. Eventhouse maken:
   - Maak een nieuwe Eventhouse aan vanuit de optie "Create".
   - Geef het een unieke naam.
   - Koppel de stock-data eventstream aan een nieuwe tabel met de naam: stock.

4. Gegevens bekijken:
   - Open de bijbehorende KQL database.
   - Voer de query uit: `stock | take 100` om voorbeeldgegevens te zien.
   - Gebruik vervolgens een query om gemiddelde prijzen te berekenen:
     `stock | where ["time"] > ago(5m) | summarize avgPrice = avg(todecimal(bidPrice)) by symbol`

5. Dashboard bouwen:
   - Pin de bovenstaande query naar een nieuw dashboard.
   - Dashboardnaam: Stock Dashboard.
   - Wijzig de tegelvisualisatie naar een kolommendiagram.

6. Waarschuwing instellen:
   - Maak een Activator-waarschuwing aan op basis van gemiddelde prijswijzigingen.
   - Voorwaarde: wanneer avgPrice met 100 stijgt.
   - Actie: stuur een e-mailmelding.
   - Locatie: sla op als een nieuw item in de werkruimte.

7. Opruimen:
   - Verwijder de werkruimte indien het project voltooid is en de gegevens niet langer nodig zijn.

Let op:
Deze instructies zijn bedoeld voor leerdoeleinden binnen Microsoft Fabric Real-Time Intelligence.


![Schermafbeelding 2025-05-06 120832](https://github.com/user-attachments/assets/10ce536d-e358-4dc9-af1e-60789492d6e0)

![Schermafbeelding 2025-05-06 121411](https://github.com/user-attachments/assets/c992f322-281c-4bb1-b934-7102ed60d910)

![Schermafbeelding 2025-05-06 121624](https://github.com/user-attachments/assets/642779e0-9403-4037-a561-597d73ae9398)


![Schermafbeelding 2025-05-06 122410](https://github.com/user-attachments/assets/3ab49826-e714-401f-ae98-6df38f40d766)


![Schermafbeelding 2025-05-06 122613](https://github.com/user-attachments/assets/3a8f3ca3-3f09-490e-bb8a-12b89dcab158)


![Schermafbeelding 2025-05-06 123018](https://github.com/user-attachments/assets/2ac41df0-86b9-4b8d-a11f-7e3fe22ce96e)


![Schermafbeelding 2025-05-06 123102](https://github.com/user-attachments/assets/1d1879b5-48f0-4fca-a20c-21ebda9e27b9)


![Schermafbeelding 2025-05-06 123209](https://github.com/user-attachments/assets/c9d4ca9f-3c3a-4cee-8bf1-63542c7a6a3f)


![Schermafbeelding 2025-05-06 123455](https://github.com/user-attachments/assets/f64bd8d0-1090-427e-835f-e790d316cfe6)


![Schermafbeelding 2025-05-06 124151](https://github.com/user-attachments/assets/87d71805-0009-442d-8a36-349bb105c32e)


![Schermafbeelding 2025-05-06 124302](https://github.com/user-attachments/assets/41252608-6668-469e-86f7-20c15ae53fbb)


![Schermafbeelding 2025-05-06 132000](https://github.com/user-attachments/assets/28778cbf-0ff0-4663-9741-d018077b15d2)

![Schermafbeelding 2025-05-06 132021](https://github.com/user-attachments/assets/78a258cb-24a2-4396-bd23-9c658f753594)


![Schermafbeelding 2025-05-06 132250](https://github.com/user-attachments/assets/6f8550c6-4346-4a3c-a164-bfed7217c09f)

![Schermafbeelding 2025-05-06 132343](https://github.com/user-attachments/assets/93d772df-566e-4f7b-9082-0d18657d9f6f)

![Schermafbeelding 2025-05-06 132546](https://github.com/user-attachments/assets/fd5697b2-1a94-4afb-9aa8-e30ab3e615b7)

![Schermafbeelding 2025-05-06 133222](https://github.com/user-attachments/assets/72805b21-5023-4ffd-b8d2-2168b8ac9546)


![Schermafbeelding 2025-05-06 133404](https://github.com/user-attachments/assets/b32f8f8f-1eba-4135-9c41-f6b0335415e4)











