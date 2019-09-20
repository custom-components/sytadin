# sytadin

_Due to [ADR0004](https://github.com/home-assistant/architecture/blob/master/adr/0004-webscraping.md) this integration was removed from [Home Assistant](https://github.com/home-assistant/home-assistant/tree/0.99.0) with version 0.100, and are now republished here._

⚠️ This integration scrapes a website to get the information!
⚠️ There are no one actively maintaining this repository.

The `sytadin` sensor platform allows you to monitor traffic details from [Sytadin](http://www.sytadin.fr).

The data is coming from the [Direction des routes Île-de-France (DiRIF)](http://www.sytadin.fr).

## Installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `sytadin`.
4. Download _all_ the files from the `custom_components/sytadin/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Restart Home Assistant.
7. Move on to the configuration.

Using your HA configuration directory (folder) as a starting point you should now also have this:

```text
custom_components/sytadin/__init__.py
custom_components/sytadin/manifest.json
custom_components/sytadin/sensor.py
```

## Example configuration.yaml

```yaml
sensor:
  - platform: sytadin
```

### Configuration options

Key | Type | Required | Description
-- | -- | -- | --
`name` | `string` | `False` | Additional name for the sensors.
`monitored_conditions` | `list` | `False` | Conditions to display in the frontend.(default is `traffic_jam`)

#### Possible `monitored_conditions`

- `traffic_jam`
- `mean_velocity`
- `congestion`

## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)
