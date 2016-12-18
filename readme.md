# (Unofficial) Locomore GTFS Feed

[General Transit Feed Specification (GTFS)](https://developers.google.com/transit/gtfs/) für [Locomore](https://locomore.com).

**Download** der .zip bei den [Releases](https://github.com/robbi5/locomore-gtfs/releases)

## Woher stammen die Angaben?

Generell stammen alle Angaben von der Locomore-Webseite und aus dem Buchungsprozess.

### agency.txt:
* `agency_id` aus https://booking.locomore.com/api/journey-search (LM, nicht LOC, wie im DB-Buchungsprozess)
* `agency_phone,agency_email` von https://locomore.com/de/kontakt/

### calendar.txt
* `start_date,end_date` von https://locomore.com/de/faq/ (Buchungszeitraum)

### routes.txt
* `route_color,route_text_color` aus dem CSS von https://locomore.com

### stops.txt:
* `stop_id,stop_code,stop_name` von https://booking.locomore.com/api/stations
* `stop_lat,stop_lon` durch Gecoding mittels https://geocoder.opencagedata.com, Daten von [OpenStreetMap](https://openstreetmap.org) contributors ([ODbL](http://opendatacommons.org/licenses/odbl/1.0/summary/))

### stop_times.txt:
* `arrival_time,departure_time` aus https://booking.locomore.com/api/journey-search

Für die Ankunftszeit/Abfahrtszeit beim ersten/letzten Stop waren diese Zeiten leider nicht verfügbar, obwohl [GTFS diese erfordert](https://developers.google.com/transit/gtfs/reference/stop_times-file):
> You must specify arrival and departure times for the first and last stops in a trip.

Locomore weiß das aktuell auch nicht:
> @locomore: @robbi5 Wie ich erfahre, gibt es bisher keine fixen Bereitstellungszeiten.  
>  ~ https://twitter.com/locomore/status/810567588896010244

Daher sind für Ankunft & Abfahrt beim ersten & letzten Stop aktuell die selben Zeiten eingetragen.

## Lizenz

[ODbL](http://opendatacommons.org/licenses/odbl/1.0/summary/)