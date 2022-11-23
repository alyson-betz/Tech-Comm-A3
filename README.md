## Sample Requests & Responses

### Getting a list of available camp sites at a specific park.

Request: 

```GET https://great-manitoba-parks.ca/campSites?name=Birds Hill&start=4/20/22&end=4/21/22``` 

Response: 
```yaml
[
  {
    name: "East 1",
    lat: 12.2883,
    long: 23.3939,
    hasElectricity: true,
    hasWater: false,
    hasFirepit: true,
  },
  {
    name: "West 4",
    lat: 14.2883,
    long: 22.3939,
    hasElectricity: true,
    hasWater: true,
    hasFirepit: false,
  },
]
```

### Getting information about a park

Request: 

```GET https://great-manitoba-parks.ca/park?name=Duck Mountain``` 

Response: 
```yaml
{
  name: "Duck Mountain",
  totalCampSites: 12,
  availableCampSites: 2,
  totalHikingTrails: 8,
  hasBeach: false,
  hasLakes: true,
  phoneNumber: "+1 (204) 555-5555"
}
```
