# comuni-italiani-geocode

## Geo-Localizzazione comuni italiani
La repository nasce con lo scopo di fornire un csv che contiene la geolocalizzazione di tutti i comuni italiani, in notazione Latitudine e Longitudine.

Il file é [questo](https://github.com/gnekt/comuni-italiani-geocode/blob/main/comuni_geocoded.csv)

I dati non collegati alla parte geografica sono stati presi da questa [repository](https://github.com/matteocontrini/comuni-json).

#### Come ho acquisito latitudine e longitudine?
Ho usato questo [servizio](https://www.mapbox.com/) che in versione free ti permette di effettuare max. 10e5 chiamate alle loro api, vi risparmio la rottura di registrarvi e di interfacciarvi con i loro servizi.

Le chiamate sono state formattate secondo questo formato:
```
    https://api.mapbox.com/geocoding/v5/mapbox.places/{comune},{cap},Italia.json?access_token={}
```
Le informazioni usate, almeno in prima battuta, sembrano essere sufficienti per permettere al loro motore di ricerca di discriminare correttamente i vari comuni.

#### Perché __MapBox__ e non altri servizi?
MapBox é stato l'unico servizio che restitutiva triangolazioni differenti anche per multi-cap appartenenti allo stesso comune.
>> In che senso?
>> Nel senso che se prendiamo il comune di Napoli(NA) come esempio, troviamo associato ad esso 27 CAP differenti.

---

### Nota bene
I dati vanno presi "as it is", ovvero che:
1) I dati __Non sono stati validati__.
2) I dati __Non sono ufficiali__.
3) Non ho modo di controllare a mano se tutte le geolocalizzazioni sono corrette.
