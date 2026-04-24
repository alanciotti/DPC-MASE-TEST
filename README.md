# Anagrafica OSS


Il file prodotto è un **GeoJSON [RFC 7946](https://datatracker.ietf.org/doc/html/rfc7946)**:

- Radice: `type` = `"FeatureCollection"`.
- `features`: un elemento per ogni **stazione attiva** inclusa nel dataset.

Ogni **feature** ha:

| Parte | Contenuto |
|--------|-----------|
| `geometry` | Punto WGS84: `type` = `"Point"`, `coordinates` = `[longitudine, latitudine]` (ordine GeoJSON standard). |
| `properties` | Dati anagrafici della stazione (identità, territorio, attributi tecnici, rete, ecc.) e l’elenco dei **sensori** associati. |

### Sensori

In `properties` si trovano:

- `sensors`: array di oggetti, uno per sensore collegato alla stazione.
- `sensors_count`: numero di elementi in `sensors`.

Ogni voce in `sensors` può includere, tra gli altri campi: identificativo e nome sensore, tipo/parametro misurato, unità di misura, quota, stati operativi, eventuali flag di finanziamento e **date in formato ISO** dove previsto.


## Naming del file e posizione

Il nome predefinito del file sul repository è **`anagrafica-oss.geojson`** 

## Frequenza di aggiornamento

Il file sul repository viene **rigenerato e pubblicato su GitHub su base pianificata**, con cadenza prevista di **circa ogni 48 ore** (due giorni).


