# FotoDino Locations API
The base api can be found at `https://testapi.photodino.de/`. 

`BASE_URL for =  https://testapi.photodino.de/`

## Events
GET

|Action |URL |Parameters |Response |
|--|--|--|--|
|get all events |`BASE_URL/events/` |`None`|Array with diciontaries for each event
|Get specific city |`BASE_URL/events/<event_id>` |`None` |Dictonary array of event details
Filter by  name|`BASE_URL/events/` | `{"name": "str"}` |List of all events matching name or not found message

POST

|Action |URL |Parameters |Response
|--|--|--|--|
|Create new event |`BASE_URL/events/` |[event object](#event_object) |created event json object

PUT

|Action |URL |Parameters|Response
|--|--|--|--|
|Update existing event |`BASE_URL/events/<event_id>/` | [event object](#event_object) |updated event json||object

DELETE

|Action |URL |Parameters |Response
|--|--|--|--|
|Delete event |`BASE_URL/events/<event_id>/` |`None` |`None` or `Not found`

### <a name=event_object|></a> `event_object`
|Attribute |Type |Example |Default 
|-- |-- |-- |--
|id |`int` |23 |auto
|events |`array` |[1, 3 ,4 ,5] |auto
|name |`str` |Birthday |`None`
|description |`str` | This event is a birthday party for a young boy |auto
|event_date |`date` | 22.1.2022 |auto

## Cities
GET

|Action |URL |Parameters |Response |
|--|--|--|--|
|get all cities |`BASE_URL/cities/` |`None`|Array with diciontaries for each city
|Get specific city |`BASE_URL/cities/<city_id>` |`None` |Dictonary array of city details
Filter by  name|`BASE_URL/cities/` | `{"name": "str"}` |List of all cities matching name or not found message
Filter by city code |`BASE_URL/cities/` | `{"code": "int"}` |List of all cities matching name or not found message

POST

|Action |URL |Parameters |Response
|--|--|--|--|
|Create new city |`BASE_URL/cities/` |[city object](#city_object) |created city json object

PUT

|Action |URL |Parameters|Response
|--|--|--|--|
|Update existing city |`BASE_URL/cities/<city_id>/` | [city object](#city_object) |updated city json||object

DELETE

|Action |URL |Parameters |Response
|--|--|--|--|
|Delete city |`BASE_URL/cities/<city_id>/` |`None` |`None` or `Not found`

### <a name=city_object|></a> `city_object`
|Attribute |Type |Example |Default 
|-- |-- |-- |--
|id |`int` |23 |auto
|locations |`array` |[1, 3 ,4 ,5] |auto
|name |`str` |Munich |`None`
|code |`int` |2239 |`None`
|time_added |`str` |2021-09-15T14:31:53.812939Z |auto


## Locations
GET

|Action |URL |Parameters |Response
|--|--|--|--|
|get all locations |`BASE_URL/locations/` |`None`|Array [location object](#location_object)
|Get specific location |`BASE_URL/locations/<location_id>` |`None` |one [location object](#location_object)
Filter by name|`BASE_URL/locations/` | `{"name": "str"}` |List of all locations matching name or empty list
Filter by city id |`BASE_URL/locations/` | `{"city_id": "int"}` |List of all locations belonging to the specific city or empty list
Filter by eamil |`BASE_URL/locations/` | `{"email": "str"}` |List of all locations matching email or empty list
General search|`BASE_URL/locations/` | `{"search": "str"}` |List of all locations matching search parameter or empty list


POST

|Action |URL |Parameters |Response
|--|--|--|--|
|Create new location |`BASE_URL/locations/` |json data |created [location object](#location_object)

PUT

|Action |URL |Parameters |Response
|--|--|--|--|
|Update existing location |`BASE_URL/locations/<location_id>/` |json Data |updated [location object](#location_object)

DELETE

|Action |URL |Parameters |Response
|--|--|--|--|
|Delete location |`BASE_URL/locations/<location_id>/` |`None` |`None` or `Not found`


### <a name=location_object></a> `location_object`
|Field |Type |Example |Default
|-- |-- |-- |-- |
|id |`int` |23 |auto
|location_events |`arr` |[1, 3 , 4 ,5] |auto
|name |`str` |Forst Hotel |`None`
|rent |`str` |109.49 |`None`
|email |`str` |johndoe@joecorp.de |`None`
|phone |`str` |+49 (012) 308 |`None`
|coordinates |`str` |49.045,10.442 |`None`
|street_number |`int` |65 |`None`
|street_name |`str` |Hartmannweg |`None`
|postal_code |`int` |51901 |`None`
|status |`str` |Only one of `Available`, `Unavailable`, `Active` |`Available`
|time_added |`int` |2021-09-15T18:47:23.644690Z |auto
|city |`int` |20 |`None`




