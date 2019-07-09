# timedcover
Custom cover component for Homeassistant

Just put the files under custom_components/timedcover folder.

Add your timed cover to configuration.yaml as follows:

```yaml
cover:
  - platform: timedcover
    covers:
      bedroom_cover:
        friendly_name: 'Bedroom Cover'
        open_cover:
          service: switch.turn_on
          entity_id: switch.bedroom_cover
        close_cover:
          service: switch.turn_off
          entity_id: switch.bedroom_cover
        stop_cover:
          service: switch.turn_on
          entity_id: switch.bedroom_cover_stop                  
        opening_time: XX
        closing_time: YY
        tilt_optimistic: false
```

Update the opening time(XX) and closing time(YY) in seconds. 
