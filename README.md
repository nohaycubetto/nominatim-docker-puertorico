# Nominatim Docker Puerto Rico

100% working container for [Nominatim](https://github.com/twain47/Nominatim) using Puerto Rico data.

[![](https://images.microbadger.com/badges/image/mediagis/nominatim.svg)](https://microbadger.com/images/mediagis/nominatim "Get your own image badge on microbadger.com")

Run [http://wiki.openstreetmap.org/wiki/Nominatim](http://wiki.openstreetmap.org/wiki/Nominatim) in a docker container. Clones the current master and builds it. This is always the latest version, be cautious as it may be unstable.

Uses Ubuntu 14.04 and PostgreSQL 9.3

# Update

Full documentation for Nominatim update available [here](https://github.com/twain47/Nominatim/blob/master/docs/Import_and_update.md#updates). For a list of other methods see the output of:
  ```
  docker exec -it nominatim sudo -u nominatim ./src/utils/update.php --help
  ```

The following command will keep your database constantly up to date:
  ```
  docker exec -it nominatim sudo -u nominatim ./src/utils/update.php --import-osmosis-all --no-npi
  ```
If you have imported multiple country extracts and want to keep them
up-to-date, have a look at the script in
[issue #60](https://github.com/twain47/Nominatim/issues/60).
