# L'accessibilitat a l'habitatge a Catalunya (2015–2023)

**Projecte 01 · Portafolis de Business Intelligence | Power BI**

## Objectiu

Analitzar com han evolucionat la **renda familiar disponible per habitant** i el **preu mitjà mensual dels nous contractes de lloguer** als municipis catalans de 2015 a 2023. L'objectiu és comparar-ne els ritmes de creixement i identificar diferències territorials.

## El dashboard

El fitxer complet es pot descarregar a **[Housing_Catalunya.pbix](Housing_Catalunya.pbix)** i obrir amb Power BI Desktop.

El projecte consta de **tres pàgines**:

1. **Evolució i accessibilitat**: creixement de renda i lloguer, diferencial en punts percentuals i comparació amb índexs base 2015 = 100.
2. **Desigualtats territorials**: mapa municipal interactiu i rànquing dinàmic dels deu municipis on més augmenta el lloguer, condicionat a la disponibilitat de dades i a un mínim de contractes.
3. **Anàlisi comparativa de l'habitatge**: mapa de les quatre províncies de Catalunya (Barcelona, Girona, Lleida i Tarragona), quatre gràfics d'evolució 2015–2023 i una taula provincial amb el lloguer mensual ponderat pel nombre de contractes.

## Captures del quadre de comandament

### 1. Evolució i accessibilitat

Comparació de la renda disponible per habitant i del preu del lloguer, amb indicadors de variació, sèries temporals i conclusions per municipi. La captura mostra l'exemple de **l'Armentera**.

![Pàgina 1: Evolució i accessibilitat](images/01-evolucio-accessibilitat.png)

### 2. Desigualtats territorials

Mapa municipal interactiu i classificació dinàmica dels municipis amb més augment del lloguer. La captura mostra l'any **2023**.

![Pàgina 2: Desigualtats territorials](images/02-desigualtats-territorials.png)

### 3. Anàlisi comparativa provincial

Mapa provincial net amb quatre gràfics de línies (un per província) i una taula de detall per any. El lloguer provincial es calcula com a **mitjana dels preus municipals ponderada pel nombre de contractes** amb preu publicat; no s'ha de confondre amb un indicador provincial oficial sense verificar-ne la cobertura.

*Captura de la tercera pàgina pendent de pujar a `images/03-comparativa-provincial.png`.*

## Fonts de dades

- **Idescat**: renda familiar disponible bruta (RFDB) per habitant, sèrie municipal.
- **INCASÒL / Generalitat de Catalunya**: estadístiques de fiances dels contractes de lloguer, preus mitjans mensuals dels nous contractes i nombre de contractes.
- **Cartografia municipal de Catalunya**: límits municipals per a la visualització geogràfica.

## Eines i metodologia

**Power BI Desktop · Power Query · DAX · Model de dades dimensional · Visualització cartogràfica**

- Anàlisi longitudinal **2015–2023**.
- Relacions entre dimensions de municipi i any i taules de fets de renda i lloguer.
- Mesures de variació percentual, índexs i diferencials.
- Filtres interactius i rànquing recalculat segons l'any seleccionat.
- Criteri de qualitat al rànquing: **almenys 10 contractes** el 2015 i l'any seleccionat.
- Anàlisi provincial: mitjana ponderada del lloguer municipal per nombre de contractes, ometent preus no publicats.

## Resultats seleccionats (2015–2023)

| Municipi | Creixement renda/habitant | Creixement lloguer | Diferencial |
|---|---:|---:|---:|
| Igualada | +26,07 % | +56,99 % | +30,92 pp |
| Barcelona | +25,99 % | +54,62 % | +28,64 pp |
| Vic | +22,69 % | +42,77 % | +20,08 pp |

Als tres municipis, el preu mitjà dels nous contractes de lloguer va créixer més ràpidament que la renda disponible per habitant.

## Interpretació i limitacions

- La **renda disponible per habitant no és el salari ni la renda d'una llar**; comparar-ne el creixement amb el lloguer no equival a calcular l'esforç residencial real.
- Els lloguers representen **nous contractes registrats**, no tots els contractes vigents.
- No tots els municipis disposen de dades publicades per a tots dos indicadors i anys. Les absències no s'han de tractar com a zeros.
- El llindar de deu contractes evita alguns casos molt volàtils, però **no garanteix representativitat estadística**.
- Els percentatges són variacions relatives entre dos anys, no variacions del pes del lloguer sobre els ingressos de les llars.

## Estat dels recursos

El repositori inclou el fitxer PBIX i la documentació. La versió més recent, amb tres pàgines, s'ha preparat i **està pendent de substituir el PBIX anterior del repositori**. Les captures referenciades a `images/` també estan pendents de pujada.

## Autor

**Joel Subirana** — projecte personal de Business Intelligence.
