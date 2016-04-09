## NEA API Wrapper

Wrapper for the National Environment Agency of Singapore's Data API.

__Disclaimer__: This wrapper is __NOT__ an official wrapper and do not attempt to represent NEA in anyway.

### About

This wrapper has the following functions:

* get_pm25()
* get_2hr_nowcast()
* get_24hrs_forecast()
* get_4days_outlook()
* get_heavy_rain_warning()
* get_uvi()
* get_earthquake()
* get_psi_update()

All functions return an OrderedDict object which you can manipulate. The structure of the OrderedDict is the same as the original XML output.

### Register for an API Key

To get an API key, you'll have to register at [NEA's dataset API page](https://www.nea.gov.sg/api/)


### Installation

```bash
$ pip install nea_api
```

### Usage

```python
from nea_api import NEA

nea = NEA(api_key="<api key>")
results = nea.get_pm25()

# ipdb> results
OrderedDict([('channel', OrderedDict([('title', 'PM2.5 Update'), ('source', 'Airviro'), ('item', OrderedDict([('region', [OrderedDict([('id', 'rNO'), ('latitude', '1.41803'), ('longitude', '103.82000'), ('record', OrderedDict([('@timestamp', '20160406140000'), ('reading', OrderedDict([('@type', 'PM25_RGN_1HR'), ('@value', '17')]))]))]), OrderedDict([('id', 'rCE'), ('latitude', '1.35735'), ('longitude', '103.82000'), ('record', OrderedDict([('@timestamp', '20160406140000'), ('reading', OrderedDict([('@type', 'PM25_RGN_1HR'), ('@value', '27')]))]))]), OrderedDict([('id', 'rEA'), ('latitude', '1.35735'), ('longitude', '103.94000'), ('record', OrderedDict([('@timestamp', '20160406140000'), ('reading', OrderedDict([('@type', 'PM25_RGN_1HR'), ('@value', '19')]))]))]), OrderedDict([('id', 'rWE'), ('latitude', '1.35735'), ('longitude', '103.70000'), ('record', OrderedDict([('@timestamp', '20160406140000'), ('reading', OrderedDict([('@type', 'PM25_RGN_1HR'), ('@value', '26')]))]))]), OrderedDict([('id', 'rSO'), ('latitude', '1.29587'), ('longitude', '103.82000'), ('record', OrderedDict([('@timestamp', '20160406140000'), ('reading', OrderedDict([('@type', 'PM25_RGN_1HR'), ('@value', '30')]))]))])])]))]))])
```

### Todo

* Tests!

### Reference

* [NEA Developers Guide](https://www.nea.gov.sg/docs/default-source/api/developer's-guide.pdf?sfvrsn=2)
