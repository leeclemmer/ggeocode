# ggeocode

Wrapper for the Google Geocoder V3 API. Read the [Google Geocoder API documentation][https://developers.google.com/maps/documentation/geocoding/] for further details on what kind of requests are possible.

## Usage

```python
	from ggeocode import GGeocode
	address = '1600 Amphitheatre Parkway, Mountain View, CA'
	gg = GGeocode(address=address)
	print gg.lat # 37.42291810
	print gg.lon # -122.08542120

	# Reverse lookup
	coords = '37.42291810,-122.08542120'
	gg = GGeocode(latlng=coords)
	print gg.address # '1600 Amphitheatre Pkwy, Mountain View, CA 94043, USA'

	# Also available
	print gg.status # 'OK'
	print gg.results # [*result1*,*result2*]
	print gg.results_count # 2
```
