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

## Esempio del dataset


<pre> ```{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [
          10.153598,
          44.23887
        ]
      },
      "properties": {
        "id": 1,
        "net_staz_name": "01CCO",
        "nome": "Chiesa di S. Caterina V.M. a Collegnago  di Fivizzano",
        "network": "GeoSIG",
        "regione": "TOSCANA",
        "provincia": "MASSA-CARRARA",
        "comune": "FIVIZZANO",
        "indirizzo": "Loc. Collegnago",
        "tipologia": "Edificio Monumentale in muratura",
        "id_tipologia": 2,
        "classificazione": "ALTRO EDIFICIO",
        "sistema": "DETTAGLIATO",
        "connessione": "Rete Dati",
        "ip": "192.168.65.2",
        "zona_sismica": 2,
        "stato": "A",
        "nome_checkmk": null,
        "fem": "SI",
        "f1": 3,
        "f2": 3,
        "f3": "5.360",
        "acquisitore_serial_number": "300012",
        "acquisitore_centralina": "CR-7",
        "acquisitore_soglia_trigger_g": "0,001",
        "sensors": [
          {
            "id_sensore": 24,
            "nome_sensore": "01CCO_AC01",
            "canali_sensore": "1, 2, 3",
            "tipo_sensore": "Triassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "0.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 25,
            "nome_sensore": "01CCO_AC02",
            "canali_sensore": "4, 5",
            "tipo_sensore": "Biassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "21.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 26,
            "nome_sensore": "01CCO_AC03",
            "canali_sensore": "6, 7",
            "tipo_sensore": "Biassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "27.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 27,
            "nome_sensore": "01CCO_AC04",
            "canali_sensore": "8, 9",
            "tipo_sensore": "Biassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "33.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 28,
            "nome_sensore": "01CCO_AC05",
            "canali_sensore": "10",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "5.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 29,
            "nome_sensore": "01CCO_AC06",
            "canali_sensore": "11",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "5.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 30,
            "nome_sensore": "01CCO_AC07",
            "canali_sensore": "12",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "15.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 31,
            "nome_sensore": "01CCO_AC08",
            "canali_sensore": "13",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "21.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 32,
            "nome_sensore": "01CCO_AC09",
            "canali_sensore": "14",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "15.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 33,
            "nome_sensore": "01CCO_AC10",
            "canali_sensore": "15",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "15.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 34,
            "nome_sensore": "01CCO_AC11",
            "canali_sensore": "16",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "15.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 35,
            "nome_sensore": "01CCO_AC12",
            "canali_sensore": "17",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "15.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 36,
            "nome_sensore": "01CCO_AC13",
            "canali_sensore": "18",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "15.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 37,
            "nome_sensore": "01CCO_AC14",
            "canali_sensore": "19",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "15.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 38,
            "nome_sensore": "01CCO_AC15",
            "canali_sensore": "20",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "17.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 39,
            "nome_sensore": "01CCO_AC16",
            "canali_sensore": "21",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "15.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 40,
            "nome_sensore": "01CCO_AC17",
            "canali_sensore": "22",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "27.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 41,
            "nome_sensore": "01CCO_AC18",
            "canali_sensore": "23",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "33.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 42,
            "nome_sensore": "01CCO_AC19",
            "canali_sensore": "24",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "17.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 43,
            "nome_sensore": "01CCO_AC20",
            "canali_sensore": "25",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "17.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          },
          {
            "id_sensore": 44,
            "nome_sensore": "01CCO_AC21",
            "canali_sensore": "26",
            "tipo_sensore": "Monoassiale",
            "parametro_misurato_sensore": "Accelerazione",
            "unita_misura_sensore": "g",
            "quota_sensore": "17.00",
            "stato_sensore": "ATTIVO",
            "stato_funzionamento_sensore": "OPERATIVO",
            "finanziato_mase": "NO",
            "data_attivazione_sensore": null,
            "data_dismissione_sensore": null,
            "ultima_lettura_sensore": null
          }
        ],
        "sensors_count": 21
      }
    }``` </pre>
