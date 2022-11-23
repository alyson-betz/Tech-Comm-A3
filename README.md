
# Provincial Park Information API 
These are 2 APIs that shows you information about Manitoba's Provincial Parks. 
1. Campground Search API 
   * The first API is a campground search API. You will be able to search for available campsites in a specific Provincial Park. All you need is the park name at which you're interested in staying, the start date of your stay, and the end date.  
2. Specific Park Information API
   * The second API gives you detailed information about a specific park. 
   * You provide the name of Provincial Park and the API will return interesting information about that park. 

## Description of resources  
   1. Campground Search API
   * Returns a list of available campsites and information about these campsites  
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
  * Return information about the requested park  
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
  

  
