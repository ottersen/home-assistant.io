---
layout: page
title: "World Tides"
description: "Instructions on how to add Tides information to Home Assistant."
date: 2017-08-23 08:00
sidebar: true
comments: false
sharing: true
footer: true
logo: worldtidesinfo.png
ha_category: Weather
ha_release: 0.52
---

The `worldtidesinfo` sensor platform uses details from [World Tides](https://www.worldtides.info/) to provide information about the prediction for the tides for any location in the world. 

## {% linkable_title Setup %}

Get your API key from your account at [https://www.worldtides.info/](https://www.worldtides.info/).

## {% linkable_title Configuration %}

To use this sensor, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
sensor:
  - platform: worldtidesinfo
    api_key: YOUR_API_KEY
```

{% configuration %}
api_key:
  description: Your API key.
  required: true
  type: string
name:
  description: Name to use in the frontend.
  required: false
  type: string
  default: WorldTidesInfo
latitude:
  description: Latitude of the location to display the tides.
  required: false
  type: float
  default: "The latitude in your `configuration.yaml` file."
longitude:
  description: Longitude of the location to display the tides.
  required: false
  type: float
  default: "The longitude in your `configuration.yaml` file."
{% endconfiguration %}

