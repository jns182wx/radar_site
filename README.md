# PA NEXRAD Radar Coverage Research

**jns182wx · Camp Hill, PA**

Interactive analysis of WSR-88D beam geometry and precipitation coverage across south-central Pennsylvania.

## Site Structure

| File | Description |
|------|-------------|
| `index.html` | Main landing page — navigation hub |
| `pa_radar_map.html` | All 67 PA counties by best radar |
| `pa_radar_coverage.html` | County beam height dashboard |
| `pa_towns_radar.html` | 26-town south-central PA reference |
| `beam_height_table.html` | ASOS station beam heights (4 tilts × 4 radars) |
| `radar_precip_v3.html` | Precipitation coverage infographic |
| `storm_jan25.html` | Jan 25 deep dive |
| `storm_mar11.html` | Mar 11 deep dive |
| `storm_mar06.html` | Mar 6 deep dive |
| `storm_mar27.html` | Mar 27 deep dive |
| `storm_feb20.html` | Feb 20 deep dive |
| `data/` | CSV and JSON datasets |

## Key Finding

Precipitation totals from ASOS `p01i` field must use **MAX per clock hour**, not sum.
The field is a running cumulative since the last routine (:56) observation.
Raw summation produces 1.5–2.5× inflated totals.

## Data Sources

- ASOS: IEM Iowa State University
- Soundings: IEM RAOB API (IAD + OKX, 00Z/12Z)
- RAP BUFKIT: IEM mtarchive
- Beam formula: 4/3 Earth-radius WSR-88D standard
