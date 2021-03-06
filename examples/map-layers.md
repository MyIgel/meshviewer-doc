# Map layers

List of map layers for your meshviewer.

{% method %}
### Freifunk Regensburg Layer

Ask us friendly and you can use our layers. Compared to Standard OSM our tiles are 30-50% smaller means less traffic.

| Key | Value |
| :--- | :--- |
| Recommend | yes |
| Style | simple & night |
| HTTP/2 | yes |
| Retina tiles | yes |
| Tracking | no |

{% sample lang="js" %}
```js
  {
      "name": "Freifunk Regensburg",
      // Please ask Freifunk Regensburg before using its tile server - example with retina tiles
      "url": "https://{s}.tiles.ffrgb.net/{z}/{x}/{y}{retina}.png",
      "config": {
        "maxZoom": 20,
        "subdomains": "1234",
        "attribution": "<a href=\"http://www.openmaptiles.org/\" target=\"_blank\">&copy; OpenMapTiles</a> <a href=\"http://www.openstreetmap.org/about/\" target=\"_blank\">&copy; OpenStreetMap contributors</a>",
        "start": 6
      }
    },
```

#### Night style

{% sample lang="js" %}
```json

    {
      "name": "Freifunk Regensburg Night",
      // Please ask Freifunk Regensburg before using its tile server - example with retina and dark tiles
      "url": "https://{s}.tiles.ffrgb.net/n/{z}/{x}/{y}{retina}.png",
      "config": {
        "maxZoom": 20,
        "subdomains": "1234",
        "attribution": "<a href=\"http://www.openmaptiles.org/\" target=\"_blank\">&copy; OpenMapTiles</a> <a href=\"http://www.openstreetmap.org/about/\" target=\"_blank\">&copy; OpenStreetMap contributors</a>",
        "mode": "night",
        "start": 19,
        "end": 
      }
    }
```
{% endmethod %}

{% method %}
### OpenStreetMap FR - Hot style

| Key | Value |
| :--- | :--- |
| Recommend | yes |
| Style | hot & others |
| HTTP/2 | no |
| Retina tiles | no |
| Tracking | unknown |

{% sample lang="js" %}
```json

    {
      "name": "OpenStreetMap.HOT",
      "url": "https://{s}.tile.openstreetmap.fr/hot/{z}/{x}/{y}.png",
      "config": {
        "maxZoom": 19,
        "attribution": "&copy; Openstreetmap France | &copy; <a href=\"http://www.openstreetmap.org/copyright\">OpenStreetMap</a>"
      }
    }
```
{% endmethod %}

{% method %}
### HERE Map

| Key | Value |
| :--- | :--- |
| Recommend | no - limit is to low, nice satellite view available |
| Style | normal & satellite |
| HTTP/2 | no |
| Retina tiles | no |
| Tracking | unknown |

{% sample lang="js" %}
Requries API token - free account with limited views available.

```json

    {
      "name": "HERE",
      // Please use your own API key - Free plan is on right side after the pay plans
      "url": "https://{s}.base.maps.api.here.com/maptile/2.1/maptile/newest/normal.day/{z}/{x}/{y}/256/png8?app_id=YOUR_KEY&app_code=YOUR_CODE&lg=deu",
      "config": {
        "attribution": "Map &copy; 1987-2014 <a href=\"http://developer.here.com\">HERE</a>",
        "subdomains": "1234",
        "maxZoom": 20
      }
    }
```
{% endmethod %}

{% method %}
#### Satellite hybrid View

{% sample lang="js" %}
```json
    {
      "name": "HERE.hybridDay",
      // Please use your own API key - Free plan is on right side after the pay plans
      "url": "https://{s}.aerial.maps.api.here.com/maptile/2.1/maptile/newest/{variant}/{z}/{x}/{y}/256/png8?app_id=YOUR_KEY&app_code=YOUR_CODE&lg=deu",
      "config": {
        "attribution": "Map &copy; 1987-2014 <a href=\"http://developer.here.com\">HERE</a>",
        "subdomains": "1234",
        "variant": "hybrid.day",
        "maxZoom": 20
      }
    }
```
{% endmethod %}

{% method %}
### Satellite map

| Key | Value |
| :--- | :--- |
| Recommend | no - slow |
| Style | normal & satellite |
| HTTP/2 | no |
| Retina tiles | no |
| Tracking | unknown |



{% sample lang="js" %}
```json

    {
      "name": "Esri.WorldImagery",
      "url": "//server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}",
      "config": {
        "maxZoom": 20,
        "attribution": "Tiles &copy; Esri &mdash; Source: Esri, i-cubed, USDA, USGS, AEX, GeoEye, Getmapping, Aerogrid, IGN, IGP, UPR-EGP, and the GIS User Community"
      }
    },
    ```
{% endmethod %}
