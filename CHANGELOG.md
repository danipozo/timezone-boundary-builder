## Unreleased

### Zone Changes

* Directly use OpenStreetMap timezone relations for the following zones:
  * `America/Denver`
  * `America/Los_Angeles`
  * `America/North_Dakota/Beulah`
  * `America/North_Dakota/Center`
  * `America/North_Dakota/New_Salem`
  * `America/Phoenix`
* Update to latest OSM data

### Other Changes

* Fix linting errors

## 2021c

### Zone Changes

* Allow additional disputed areas to overlap ([#105](https://github.com/evansiroky/timezone-boundary-builder/issues/105))
  * `Africa/Ouagadougou`, `Africa/Porto-Novo` overlap. See [article](https://fr.wikipedia.org/wiki/Koalou).
  * `America/Lower_Princes`, `America/Marigot` overlap. See [article](http://www.dclportal.dreamhosters.com/news/latest-news/9228-negotiations-on-oyster-pond-border-to-commence-late-2019).
  * `America/Nuuk`, `America/Pangnirtung` overlap. See [article](https://en.wikipedia.org/wiki/Hans_Island).
  * `America/Sitka`, `America/Vancouver` overlap. See [article](https://en.wikipedia.org/wiki/Dixon_Entrance#Boundary_dispute).
  * `Asia/Bangkok`, `Asia/Yangon` overlap. See [article](https://en.wikipedia.org/wiki/Myanmar%E2%80%93Thailand_relations#Disputed_territory).
  * `Asia/Hebron`, `Asia/Jerusalem` overlap in Area H2. See [article](https://en.wikipedia.org/wiki/Hebron#Division_of_Hebron)
  * `Asia/Kolkata`, `Asia/Shanghai` overlap. See [article](https://en.wikipedia.org/wiki/Sino-Indian_border_dispute).
  * `Europe/Athens`, `Europe/Istanbul` overlap. See [article](https://en.wikipedia.org/wiki/Imia/Kardak).
* Ensure territorial waters are included in the following zones:
  * `Asia/Srednekolymsk`
  * `Australia/Adelaide`
  * `Australia/Brisbane`
  * `Australia/Darwin`
  * `Australia/Eucla`
  * `Australia/Hobart`
  * `Australia/Lindeman`
  * `Australia/Melbourne`
  * `Australia/Perth`
  * `Australia/Sydney`
* Merge some zones that were moved to the backzone file in the timezone database
  * `Australia/Currie` is now a part of `Australia/Hobart`
* Rename `Pacific/Enderbury` to `Pacific/Kanton`
* Rely mostly on OSM timezone relations for `America/Chicago` and `America/New_York` ([#123](https://github.com/evansiroky/timezone-boundary-builder/issues/123)).
* Update to latest OSM data

### Other Changes

* Change output folder of various files outputted from building script ([#102](https://github.com/evansiroky/timezone-boundary-builder/pull/102)).
* Update list of libraries using data ([#110](https://github.com/evansiroky/timezone-boundary-builder/issues/110), [#111](https://github.com/evansiroky/timezone-boundary-builder/pull/111))
* Update all dependencies and require at least node 12.
* Begin using a standard naming practice for timezone relations in `osmBoundarySources.json`.
* Add note about intent to rely more on timezone data directly from OpenStreetMap.

## 2020d

### Zone Changes

* Update some Canadian zones as follows ([#90](https://github.com/evansiroky/timezone-boundary-builder/issues/90))
  * Use OSM timezone relations in entirety for the following zones: `America/Blanc_Sablon`, `America/Glace_Bay`, `America/Halifax`, `America/Swift_Current`, `America/Toronto`
* Add disputed area along Northwest Bhutan-China border.
* Manually add back the Jungholz Village to `Europe/Vienna` ([#93](https://github.com/evansiroky/timezone-boundary-builder/issues/93)).
* Update to latest OSM data

### Other Changes

* Switch command line flag processing to use the yargs library. Existing flags have changed: ``--no-validation` and ``--filtered-zones` have been renamed to ``--skip_validation` and `--included_zones` respectively. `--included_zones` now takes a list without quotes or commas.
* Addition of new flags: `--excluded_zones`, `--dist_dir`, `--downloads_dir`, `--skip_analyze_diffs`, `--skip_shapefile`, `--skip_zip`. See `--help` and README.md for details.
* Remove unneeded downloaded files from downloads directory before creating input data zipfile ([#82](https://github.com/evansiroky/timezone-boundary-builder/issues/82)).
* Junk directory names when zipping data for releases
* Add ability to generate a difference of the zone boundaries between the current config and the latest release. ([#83](https://github.com/evansiroky/timezone-boundary-builder/issues/83)).

## 2020a

### Zone Changes

* Allow timezones `Asia/Tbilisi` and `Europe/Moscow` to overlap
* Rename `America/Godthab` to `America/Nuuk` ([#77](https://github.com/evansiroky/timezone-boundary-builder/issues/77))
* Update some Canadian zones as follows ([#76](https://github.com/evansiroky/timezone-boundary-builder/issues/76))
  * Make Listuguj part of `America/Halifax` instead of `America/Moncton`
  * Make `America/Nipigon` comprise of most of mid-Ontario. _Credit to OSM user [Arctic gnome](https://www.openstreetmap.org/user/Arctic%20gnome) for OSM edits._
  * Make `America/Rainy_River` comprise of the Westernmost parts of Ontario bordering Manitoba. _Credit to OSM user [Arctic gnome](https://www.openstreetmap.org/user/Arctic%20gnome) for OSM edits._
  * Split Northwest Territories timezones (`America/Inuvik` and `America/Yellowknife`) in two using 120th meridian
  * Make `America/Swift_Current` comprise of all areas in southwest Saskatchewan between the `America/Regina` and `America/Edmonton` timezones.
  * Split Yukon timezones (`America/Dawson` and `America/Whitehorse`) in two using 138th meridian
* Update to latest OSM data

### Other Changes

* Update packages to latest versions
* Include input data in release files ([#78](https://github.com/evansiroky/timezone-boundary-builder/issues/78))

## 2019b

### Zone Changes

* Update to latest OSM data

### Other Changes

* Include JSON list of timezone names in each release ([#69](https://github.com/evansiroky/timezone-boundary-builder/issues/69))
* Improve troubleshooting wiki by adding demo video on fixing broken relations ([#68](https://github.com/evansiroky/timezone-boundary-builder/issues/68))

## 2019a

### Zone Changes

* Split Vietnam into 2 zones ([#66](https://github.com/evansiroky/timezone-boundary-builder/issues/66))
  * Make Northern Vietnam be a part of `Asia/Bangkok`
  * Southern Vietnam stays `Asia/Ho_Chi_Minh`
* Make Bir Tawil area be a part of `Africa/Cairo` instead of being a part of `Africa/Khartoum`.
* Update to latest OSM data

### Other Changes

* Add standard linter ([#67](https://github.com/evansiroky/timezone-boundary-builder/issues/67))

## 2018i

### Zone Changes

* Make territories of Taiwan take precedence when they overlap Chinese-claimed territories.  ([#52](https://github.com/evansiroky/timezone-boundary-builder/issues/52))
* Add Oslo Accords Area B and C to `Asia/Jerusalem`.  ([#53](https://github.com/evansiroky/timezone-boundary-builder/issues/53))
* Create new zone `Asia/Qostanay` by taking area from `Asia/Qyzylorda`.  ([#59](https://github.com/evansiroky/timezone-boundary-builder/issues/59))
* Change timezone for Antarctic Station Neumayer III Station from `Europe/Berlin` to `Etc/UTC`.  ([#61](https://github.com/evansiroky/timezone-boundary-builder/issues/61))
* Update to latest OSM data

### Other Changes

* Add some badges to the README
* Add progress stats reporting
* Update to use Node 10 ([#56](https://github.com/evansiroky/timezone-boundary-builder/issues/56))

## 2018g

### Zone Changes

* Switch geometries of `America/Danmarkshavn` and `America/Scoresbysund` ([#40](https://github.com/evansiroky/timezone-boundary-builder/issues/40))
* Add timezones in Antarctica ([#42](https://github.com/evansiroky/timezone-boundary-builder/issues/42))
* Fix northern border of `America/Argentina/Rio_Gallegos` ([#46](https://github.com/evansiroky/timezone-boundary-builder/issues/46))
* Allow timezone boundaries to overlap. ([#41](https://github.com/evansiroky/timezone-boundary-builder/issues/41))
  * This change now means that the following zones overlap:
    * `Africa/Juba`, `Africa/Khartoum`
    * `America/Argentina/Rio_Gallegos`, `America/Punta_Arenas`
    * `America/La_Paz`, `America/Porto_Velho`
    * `America/Moncton`, `America/New_York`
    * `Asia/Hebron`, `Asia/Jerusalem`
    * `Asia/Ho_Chi_Minh`, `Asia/Manila`
    * `Asia/Ho_Chi_Minh`, `Asia/Shanghai`
    * `Asia/Manila`, `Asia/Shanghai`
    * `Asia/Shanghai`, `Asia/Taipei`
    * `Asia/Shanghai`, `Asia/Urumqi`
    * `Europe/Amsterdam`, `Europe/Berlin`
    * `Europe/Belgrade`, `Europe/Zagreb`
    * `Europe/Berlin`, `Europe/Luxembourg`
    * `Europe/Paris`, `Europe/Rome`
* Add disupted area near Doklam to `Asia/Shanghai` and `Asia/Thimphu` ([#49](https://github.com/evansiroky/timezone-boundary-builder/issues/49))
* Update boundaries of `America/Creston` and `America/Edmonton` to reflect changes in OpenStreetMap
* Update to latest OSM data

### Other Changes

* Added more libraries to list of lookup libraries using this project's data
* Fixed overpass querying ([#43](https://github.com/evansiroky/timezone-boundary-builder/issues/43))

## 2018d

### Zone Changes

* Add timezones in the oceans ([#34](https://github.com/evansiroky/timezone-boundary-builder/issues/34))
  * Shapefiles and geojson are now outputted as with or without oceans
* Fix Viedma Glacier are to reflect latest OSM boundaries
* Update to latest OSM data

### Other Changes

* Better debugging
  * Printing Overpass query for when no data is received.
  * Using geojsonhint and writing problematic geojson to a pretty-printed file.
  * Save validation overlaps to file.
  * Add links to troubleshooting wiki for common errors.
* Update README
  * Add list of geographical lookup libraries
  * Add troubleshooting wiki

## 2017c

### Zone Changes

* Refactor of timezones in China ([#13](https://github.com/evansiroky/timezone-boundary-builder/issues/13))
  * Integration of areas formerly found in Asia/Chongqing, Asia/Harbin and Asia/Kashgar into other zones
  * Expansion of Asia/Shanghai to all of China except Xinjiang
  * Asia/Urumqi is now comprised of Xinjiang
* Fix Mexico Beach, FL by moving it to central time ([#20](https://github.com/evansiroky/timezone-boundary-builder/issues/20))
* Make Viedma glacier area work with updated OSM boundaries
* Remove small holes and reduce geojson precision. ([#11](https://github.com/evansiroky/timezone-boundary-builder/issues/11) and [#17](https://github.com/evansiroky/timezone-boundary-builder/issues/17))
* Remove zones found in backward file of timezone db ([#16](https://github.com/evansiroky/timezone-boundary-builder/issues/16))
  * America/Coral_Harbour now integrated into America/Atikokan
  * America/Montreal now integrated into America/Toronto
  * See notes on China refactor for changes to Asia/Chongqing, Asia/Harbin, Asia/Kashgar, Asia/Shanghai and Asia/Urumqi
  * Asia/Rangoon renamed to Asia/Yangon
  * Pacific/Yap integrated into Pacific/Chuuk
  * Pacific/Johnston integrated into Pacific/Honolulu
* Refactor arbitrary sea boundaries of timezones in the Gulf of St Lawrence to account for updated OSM geometry of the boundary of Quebec.
* Add Page, AZ to America/Phoenix ([#9](https://github.com/evansiroky/timezone-boundary-builder/issues/9))
* Update to latest OSM data

### Other Changes

* Add linting of json files
  * A overpass source listed in timezones.json must have a corresponding definition in osmBoundarySources.json
  * A overpass source defined in osmBoundarySources.json must be used in at least one operation in timezones.json
  * A manual-polygon or manual-multipolygon defined in timezones.json must be accompanied with a description.
* Add ability to build only certain zones in builder script
* Add travis-ci builds that require linting script to pass
* Added descriptions to manual geometries
* Add ability to use overpass to fetch ways that represent boundaries
* Rewrite README

## 2017a

* Zone Changes
  * Add new zone America/Punta_Arenas by taking area from America/Santiago
  * Move the boundary of America/New_York and America/Chicago in the region of various towns in Alabama such as Phenix City to the west to include these towns in America/New_York
  * Implement own interpretation of border of America/Chicago and America/Denver in the following places:
    * Move boundary to the east of ND Highway 31 in Sioux county, ND
    * Move diagonal boundary through Stanley County, SD northwest so it doesn't go through the middle of Fort Pierre
  * Update to latest OSM data
* Other changes
  * Add picture of zones to README

## 2016j

- Zone Changes
  - Add new zone Asia/Atyrau by taking area from Asia/Aqtau
  - Add new zone Europe/Saratov by taking area from Europe/Volgograd
  - Update to latest OSM data
- Other changes
  - README updates


## 2016i

- Zone Changes
  - Split Cyprus into 2 zones.  The existing Asia/Nicosia now ends at
    the northern boundary of the United Nations Buffer Zone and the new
    zone Asia/Famagusta contains everything north of the buffer zone.
  - Add missing data definitions: Congo-Kinshasa and South Sudan
  - Old Crimea boundary no longer exists in OSM, use combination of
    Crimea + Sevastopol
  - Typo of extra space in Harrison County fixed in OSM
  - Taishan City now has invalid geometry in OSM, use Xinhui district
    instead when making boundaries
  - Update to latest OSM data
- Other changes
  - Add download throttling of publicly available Overpass API
  - Remove old dist files if they exist so ogr2ogr can work
  - Update README to note change in Overpass API querying


## 2016d

First data release of the project.
