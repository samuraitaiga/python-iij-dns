# python library(API wrapper) for IIJ DNS service
python library which can easily manage [IIJ DNS Service API](http://manual.iij.jp/dns/doapi/ "DO-API Reference").

## Note
 - currently supports only
   - [get all zones](http://manual.iij.jp/dns/doapi/754466.html "GET ZONES")
   - [get record in specific zone](http://manual.iij.jp/dns/doapi/754503.html "GET RECORD)

## required
 - python 2.7+
 - pip
 - urllib3
 - PyYAML

## install
1. install by pip
```sh
# pip install iijdns
```

## Example
```python
ACCESS_KEY = 'XXXXXXX'
SECRET_KEY = 'YYYYYYY'
SERVICE_CODE = 'doZZZZZZZ'
from iijdns.dns import initialize, get_zones, get_records
initialize(ACCESS_KEY, SECRET_KEY, SERVICE_CODE)
# get all zones by array of zone( dict parsed from json) .
json_zones = get_zones()
# get record in specific zone.
json_records = get_records(r'www.example.com')
```
