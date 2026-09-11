# H.A.R.D. Aquatics — Pool Relay embed preview

An unofficial replica of the Hayward Area Recreation and Park District **Aquatics** page with
live [Pool Relay](https://www.poolrelay.com) calendars for the **Arroyo Swim Center** and the
**Hayward Plunge**.

**This is not a H.A.R.D. website.** The official page is
<https://www.haywardrec.org/238/Aquatics>. This is a working preview of one proposed change
to it, and the page says so in a ribbon across the top.

## Why two calendars

The district's aquatics director confirmed that **Arroyo is staying open through September
until the Plunge reopens in early October**. The page shows both, and the handover is simply
what the dates say:

- **Arroyo** — open now, six lanes, full today.
- **The Plunge** — empty today because the pool is closed, with its whole fall schedule
  already loaded from 3 October. Step forward with the arrows and nineteen lanes fill up.

A closed pool showing as a closed pool is the point: nobody has to remember to take one
schedule down and put the next one up on the right morning.

## Data check before building

The modelled Arroyo schedule was compared cell by cell against the district's own facility
page. Saturday, Sunday, the evening block and Aqua-Robix all matched. Two weekday blocks did
not, and were corrected to what H.A.R.D. publishes:

| | was | now |
|---|---|---|
| Weekday morning | 6:00–8:30am | **6:00–8:45am** |
| Weekday midday | 11:30am–1:00/2:00pm | **10:30am–1:00pm** |
| Friday evening | 4:00–7:00pm | **5:00–7:00pm** |

Each series now records its source and the date it was read.

**Worth knowing:** the aquatics *overview* page still describes Arroyo as one of "three
seasonal facilities that are open from June to early August", while Arroyo's *own* facility
page carries a current schedule with a "Closed: Labor Day" note. The two disagree — which is
itself part of the pitch.

```html
<iframe src="https://www.poolrelay.com/embed/I7oc1OICLuHsDCidjXmVMh" ... ></iframe>  <!-- Arroyo -->
<iframe src="https://www.poolrelay.com/embed/TDhRrzOg09V15YJQAhwi2V" ... ></iframe>  <!-- Plunge -->
```

## Notes

- The H.A.R.D. badge is a CSS placeholder, not the district's mark.
- Navigation links point at the live site. `noindex` is set.

## Local preview

```
python3 -m http.server 8809
```
