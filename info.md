# sytadin

_Due to [ADR0004](https://github.com/home-assistant/architecture/blob/master/adr/0004-webscraping.md) this integration was removed from [Home Assistant](https://github.com/home-assistant/home-assistant/tree/0.99.0) with version 0.100, and are now republished here._

⚠️ This integration scrapes a website to get the information!
⚠️ There are no one actively maintaining this repository.

The `sytadin` sensor platform allows you to monitor traffic details from [Sytadin](http://www.sytadin.fr).

The data is coming from the [Direction des routes Île-de-France (DiRIF)](http://www.sytadin.fr).

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
