
# Provincial Park Information API 
These are 2 APIs that shows you information about Manitoba's Provincial Parks. 
1. Campground Search API 
   * The first API is a campground search API. You will be able to search for available campsites in a specific Provincial Park. All you need is the park name at which you're interested in staying, the start date of your stay, and the end date.  
2. Specific Park Information API
   * The second API gives you detailed information about a specific park. 
   * You provide the name of Provincial Park and the API will return interesting information about that park. 
   
## List of Endpoints with Parameters

### ```GET /campSites?name=&start=&end=```

**name**: Name of the Provincial Park located in Manitoba for which you want to check campsite availability. (Required)  
**start**: Starting date from when you want to check-in to the campsite. In mm/dd/yyyy format. (Required)  
**end**: Ending date from when you want to check-out of the campsite. In mm/dd/yyyy format. (Required)  


### ```GET /park?name=```   

**name**: Name of the Provincial Park located in Manitoba for which you want information.


## Description of resources  
   1. Campground Search API
   Returns a list of available campsites and information about these campsites  
   ```yaml
   [  
    {  
      name: string,  
      lat: number,  
      long: number,  
      hasElectricity: boolean,  
      hasWater: boolean,  
      hasFirepit: boolean,  
    }, 
    ...  
  ]   
  ```
  2. Specific Park Information API
  Return information about the requested park  
  ```yaml
  {  
    name: string,  
    totalCampSites: number,  
    availableCampSites: number,  
    totalHikingTrails: number,  
    hasBeach: boolean,  
    hasLakes: boolean,  
    phoneNumber: string  
  }  
```
  
## Sample Requests & Responses

### Getting a list of available camp sites at a specific park.

**Request**:   
```https://great-manitoba-parks.ca/campSites?name=Birds Hill&start=4/20/22&end=4/21/22``` 

**Response**: 
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

**Request**:  
```https://great-manitoba-parks.ca/park?name=Duck Mountain``` 

**Response**: 
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


  
