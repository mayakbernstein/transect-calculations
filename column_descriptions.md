# Column Naming Summary

This document outlines the naming structure used for columns in the [variable calculation file](VegDataCalculations.ipynb)

## Column Types and Naming Patterns

| Column Type                 | Naming Formula                 | Description                                                                     |
|-----------------------------|--------------------------------|---------------------------------------------------------------------------------|
| Transect Metadata           | `transect`, `sitename`, `date` | Basic site and transect-level information.                                      |
| Length                      | `<ZONE>_length`                | the total positive distance (length) of the identified zone                     |
| Cover Summary Columns       | `pctcov_<CATEGORY>_<ZONE>`     | percent cover by category across different transect zones (whole, dune, or veg) |
| Species-Level Cover Columns | `pctcov_<CODE>_<ZONE>`         | percent cover for specific cover types in different transect zones              |

### To see the specifics on definitions for [zones], [Categories], and [Codes], see below.

## Zones

`<ZONE>` = The portion of the transect that the corresponding calculation is valid for. For percent cover calculations, the value of the denominator is determined by the zone.

| `<ZONE>`  | Description                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<whole>` | Any column with `whole` in the title means the calculation is valid for the entire transect, identified as the distance between the most inland point measured and the high tide strand line (HTS).                    |
| `<dune>`  | Any column with `dune` in the title means the calculation is valid for the portion of the transect within the foredune, identified as the distance between the inland and seaward dune toes.                           |
| `<veg>`   | Any column with `veg` in the title means the calculation is valid for the vegetated portion of the transect, identified as the distance between the most inland point measured and most seaward identified vegetation. |

## Categories {#Components}

`<CATEGORY>` = General cover group. The categories are as follows:

| `<CATEGORY>`                  | Description                                                                                                      |
|-------------------------------|------------------------------------------------------------------------------------------------------------------|
| `<all>`                       | All cover types identified                                                                                       |
| `<TerrestrialPlant>`          | Terrestrial vegetation. This includes native an nonnative vegetation.                                            |
| `<OtherCover>`                | Any cover type that does not fit into another category, other than `<all>`. ex: terrestrial debris, cobble, etc. |
| `<Wrack>`                     | Wrack. This is organic material produced by marine ecosystems washed onto the beach/dune.                        |
| `<DeadTerrestrialPlant>`      | Dead terrestrial vegetation. This is dead but identifiable terrestrial vegetation.                               |
| `<TerrestrialPlantNative>`    | Native terrestrial vegetation to California beach/dune ecosystems.                                               |
| `<TerrestrialPlantNonnative>` | Native terrestrial vegetation to California beach/dune ecosystems.                                               |
| `<TerrestrialAnimal>`         | Terrestrial animal.                                                                                              |

## Codes

`<CODE>` = Species abbreviation / cover type. See the currently identified codes below or in [CSV format](codes.csv).

| codetype           | code     | description                                                                                                                     | native |
|--------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|--------|
| Other Cover        | -D       | dead plant, this is added on to the end of another species code. ex: "CAMA-D". If it is unidentifiable, it will be marked as TD |        |
| Terrestrial Plant  | ABLA     | Abronia latifolia (Yellow sand verbena)                                                                                         | TRUE   |
| Terrestrial Plant  | ABMA     | Abronia maritima (red sand verbena)                                                                                             | TRUE   |
| Terrestrial Plant  | ABUM     | Abronia umbellata (pink sand verbena)                                                                                           | TRUE   |
| Terrestrial Plant  | ACGL     | Acmispon glaber (deerweed)                                                                                                      | TRUE   |
| Terrestrial Plant  | ACMI     | Acmispon micranthus (small-flowered lotus)                                                                                      | TRUE   |
| Terrestrial Plant  | AMAR     | Ammophila arenaria (Marram grass)                                                                                               | FALSE  |
| Terrestrial Plant  | AMCH     | Ambrosia chamissonis (beach bur)                                                                                                | TRUE   |
| Terrestrial Plant  | ANAR     | Anagallis arvensis (scarlet pimpernel)\*                                                                                        | FALSE  |
| Terrestrial Plant  | ARCA     | Artemisia californica (California Sagebrush)                                                                                    | TRUE   |
| Terrestrial Plant  | ARDO     | Arundo donax (giant reed)\*                                                                                                     | FALSE  |
| Terrestrial Plant  | ASNU     | Astragalus nuttallii (Nuttall's milkvetch)                                                                                      | TRUE   |
| Terrestrial Plant  | ATCA     | Extriplex californica (California saltbush)                                                                                     | TRUE   |
| Terrestrial Plant  | ATLE     | Atriplex leucophylla (sea scale, beach saltbush)                                                                                | TRUE   |
| Terrestrial Plant  | ATLEN    | Atriplex lentiformis (quail bush, big saltbush)                                                                                 | TRUE   |
| Terrestrial Plant  | ATPR     | Atriplex prostrata (fat-hen, spear leaved saltbush)\*                                                                           | FALSE  |
| Wrack              | B        | other brown algae                                                                                                               | FALSE  |
| Terrestrial Plant  | BAPI     | Baccharis pilularis (Coyote Brush)                                                                                              | TRUE   |
| Terrestrial Plant  | BRDI     | Bromus diandrus (Ripgut Brome)\*                                                                                                | FALSE  |
| Terrestrial Plant  | BRNI     | Brassica nigra (black mustard) \*                                                                                               | FALSE  |
| Terrestrial Plant  | BRRA     | Brassica rapa (field mustard)\*                                                                                                 | FALSE  |
| Terrestrial Plant  | BRRU     | Bromus rubens (red brome)\*                                                                                                     | FALSE  |
| Terrestrial Plant  | BRXX     | Brassica spp. \*                                                                                                                | FALSE  |
| Wrack              | C        | Cystoseria spp.                                                                                                                 | FALSE  |
| Terrestrial Plant  | CACH     | Camissoniopsis cheiranthifolia (beach evening primrose)                                                                         | TRUE   |
| Terrestrial Plant  | CAED     | Carpobrotus sp. (iceplant) \* (includes C. edulis & C. chilensis)                                                               | FALSE  |
| Terrestrial Plant  | CAMA     | Cakile maritima (sea rocket)\*                                                                                                  | FALSE  |
| Terrestrial Plant  | CASO     | Calystegia soldanella (beach morning glory)                                                                                     | TRUE   |
| Terrestrial Plant  | CAXX     | Carex spp. (sedges)                                                                                                             | FALSE  |
| Terrestrial Plant  | CHBU     | Chenopodium berlandieri (pitseed goosefoot)                                                                                     | TRUE   |
| Terrestrial Plant  | CIRH     | Cirsium rhothophilum (Surf thistle)                                                                                             | TRUE   |
| Other Cover        | CO       | Cobble                                                                                                                          |        |
| Terrestrial Plant  | COFI     | Corethrogyne filaginifolia (California aster)                                                                                   | TRUE   |
| Terrestrial Plant  | COPU     | Conicosia pugioniformis (narrow-leaf iceplant)                                                                                  | FALSE  |
| Terrestrial Plant  | CRCA     | Croton californicus (California croton)                                                                                         | TRUE   |
| Terrestrial Plant  | CYDA     | Cynodon dactylon (Bermuda grass) \*                                                                                             | FALSE  |
| Other Cover        | DF       | drift fence                                                                                                                     |        |
| Terrestrial Plant  | DISP     | Distichlis spicata (saltgrass)                                                                                                  | TRUE   |
| Terrestrial Plant  | DUCA     | Dudleya caespitosa (Coast dudleya)                                                                                              | TRUE   |
| Terrestrial Plant  | DULA     | Dudleya lanceolata (Lanceleaf liveforever)                                                                                      | TRUE   |
| Wrack              | E        | Egregia sp. (feather boa kelp)                                                                                                  | TRUE   |
| Terrestrial Plant  | ELMO     | elymus mollis (Pacific dune grass)                                                                                              | TRUE   |
| Terrestrial Plant  | ENCA     | Encelia californica (bush sunflower)                                                                                            | TRUE   |
| Terrestrial Plant  | ERBL     | Erigeron blochmaniae (Blochman's leafy daisy)                                                                                   | TRUE   |
| Terrestrial Plant  | ERBO     | Erigeron bonariensis (Flax-leaved horseweed)\*                                                                                  | FALSE  |
| Terrestrial Plant  | ERCA     | Erigeron canadensis​​​​ (Canadian horseweed)                                                                                        | TRUE   |
| Terrestrial Plant  | ERCI     | Erodium cicutarium (redstem stork's-bill)\*                                                                                     | FALSE  |
| Terrestrial Plant  | ERER     | Ericameria ericoides (mock heather)                                                                                             | TRUE   |
| Terrestrial Plant  | ERPA     | Eriogonum parvifolium (coastal buckwheat)                                                                                       | TRUE   |
| Terrestrial Plant  | ERXX     | Erodium spp. (filaree) \*                                                                                                       | FALSE  |
| Terrestrial Plant  | ESCA     | Eschscholzia californica (California Poppy)                                                                                     | TRUE   |
| Terrestrial Plant  | FRSA     | Frankenia salina (alkalai heath)                                                                                                | TRUE   |
| Other Cover        | GL       | glass                                                                                                                           |        |
| Terrestrial Plant  | HASQ     | Hazardia squarosa (sawtooth goldenbush)                                                                                         | TRUE   |
| Terrestrial Plant  | HECU     | Heliotropium curassavicum (seaside heliotrope)                                                                                  | TRUE   |
| Terrestrial Plant  | ISME     | Iscoma menziesii (goldenbush)                                                                                                   | TRUE   |
| Terrestrial Plant  | JACA     | Jaumea carnosa (Marsh Jaumea)                                                                                                   | TRUE   |
| Terrestrial Plant  | LASE     | Lactuca serriola (prickly lettuce)\*                                                                                            | FALSE  |
| Terrestrial Plant  | LUBI     | Lupinus bicolor (bicolor lupine)                                                                                                | TRUE   |
| Terrestrial Plant  | LUCH     | Lupinus chamissonis (bush lupine)                                                                                               | TRUE   |
| Terrestrial Plant  | LYAR     | Lysimachia arvensis (Scarlet pimpernel)\*(prevous ANAR)                                                                         | FALSE  |
| Wrack              | M        | Macrocystis pyrifera (giant kelp)                                                                                               | TRUE   |
| Terrestrial Plant  | MAIN     | Malacothrix incana (Dunedelion)                                                                                                 | TRUE   |
| Terrestrial Plant  | MAPA     | Malva parviflora (cheeseweed mallow)\*                                                                                          | FALSE  |
| Terrestrial Plant  | MAXX     | Malva spp. (mallow)\*                                                                                                           | FALSE  |
| Terrestrial Plant  | MEAL     | Melilotus albus (white sweetclover) \*                                                                                          | FALSE  |
| Terrestrial Plant  | MEIN     | Melilotus indicus (yellow sweetclover) \*                                                                                       | FALSE  |
| Terrestrial Plant  | MEXX     | unidentified clover species (Melilotus) \*                                                                                      | FALSE  |
| Terrestrial Plant  | MYLA     | Myoporum laetum (myoporum) \*                                                                                                   | FALSE  |
| Wrack              | N        | Nereocystis spp. (ribbon kelp)                                                                                                  |        |
| Terrestrial Plant  | NEDE     | Nemacaulis denudata (Woolly Heads)                                                                                              | TRUE   |
| Wrack              | P        | Phyllospadix torreyi (surfgrass)                                                                                                | TRUE   |
| Terrestrial Plant  | PAIN     | Parapholis incurva (sickle grass)\*                                                                                             | FALSE  |
| Terrestrial Plant  | PHRA     | Phacelia ramosissima (Branching phacelia)                                                                                       | TRUE   |
| Terrestrial Plant  | PLCO     | plantago coronopus (buck's-horn plantain)\*                                                                                     | FALSE  |
| Terrestrial Plant  | PLLA     | Plantago lanceolata (longleaf plantain)\*                                                                                       | FALSE  |
| Terrestrial Plant  | PLXX     | Plantago spp. \*                                                                                                                | FALSE  |
| Terrestrial Plant  | POAV     | Polygonum aviculare (prostrate knotweed)\*                                                                                      | FALSE  |
| Wrack              | R        | other red algae                                                                                                                 | FALSE  |
| Terrestrial Plant  | RASA     | Raphanus sativus (Wild Radish)\*                                                                                                | FALSE  |
| Terrestrial Plant  | RICO     | Ricinus communis (castor bean)\*                                                                                                | FALSE  |
| Other Cover        | RO       | fence rope                                                                                                                      |        |
| Terrestrial Animal | RODENTG  | Thomomys bottae (Botta's pocket gopher)                                                                                         | TRUE   |
| Terrestrial Animal | RODENTK  | Dipodomys heermani arenae (Heerman's kangaroo rat (Lompoc subspecies))                                                          | TRUE   |
| Terrestrial Animal | RODENTMX | unidentified mouse species                                                                                                      | TRUE   |
| Terrestrial Animal | RODENTX  | unidentified rodent species                                                                                                     | TRUE   |
| Wrack              | S        | Sargassum spp.                                                                                                                  | FALSE  |
| Terrestrial Plant  | SAPA     | Salicornia pacifica (pacific pickleweed)                                                                                        | TRUE   |
| Terrestrial Plant  | SAVI     | Salicornia virginica (common pickleweed)                                                                                        | TRUE   |
| Terrestrial Plant  | SCCA     | Schoenoplectus californicus (california bulrush)                                                                                | TRUE   |
| Terrestrial Plant  | SEBL     | Senecio blochmaniae (Blochman's groundsel, dune ragwort)                                                                        | TRUE   |
| Terrestrial Plant  | SOOL     | Sonchus oleraceus (sow thistle) \*                                                                                              | FALSE  |
| Terrestrial Plant  | SPMA     | Spergularia marina (salt sand spurry)                                                                                           | TRUE   |
| Other Cover        | T        | tar                                                                                                                             |        |
| Terrestrial Plant  | TARA     | Tamarix ramosissima (salt cedar) \*                                                                                             | FALSE  |
| Other Cover        | TD       | terrestrial debris                                                                                                              |        |
| Terrestrial Plant  | TETE     | Tetragonia tetragonoides (New Zealand spinach)\*                                                                                | FALSE  |
| Other Cover        | TR       | trash                                                                                                                           |        |
| Wrack              | U        | Ulva spp.                                                                                                                       | FALSE  |
| Other Cover        | W        | wood (large woody debris)                                                                                                       |        |
| Other Cover        | WA       | Water (pool or flooded area)                                                                                                    |        |
| Wrack              | WX       | unidentified wrack                                                                                                              | TRUE   |
| Terrestrial Plant  | XAST     | Xanthium strumarium (rough cocklebur)\*                                                                                         | FALSE  |
| Wrack              | Z        | Zostera (eelgrass)                                                                                                              | TRUE   |
| Other Cover        | GR       | gravel                                                                                                                          |        |

\*A `1` in the native column identifies that code as native, a `0` identifies the code as nonnative. Blank is not applicable NaN.
