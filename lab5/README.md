# San Francisco Bay Vessel Flow Map

# 1. Study Area and Dates
- I decided to look at the San Francisco Bay Area vessel traffic from June 10 to June 12 2025.
- Times: 17:00 PDT (June 10) to 17:59:59 PDT (June 12)
- The time zone I'm using is San Francisco Pacific Daylight Time (UTC-7). 
- I decided to use the San Francisco Bay Area since it is a deep sea floor area with heavy traffic similarly to the Puget Sound, particularly with heavy passenger vessel traffic between different major cities in the Bay Area such as San Francisco, Oakland, Richmond, Berkeley, and San Rafael. The ferries that run between these routes offer lots of visual data to be displayed through the map, and the specific dates of June 10 to June 12 were chosen as a randomized high-traffic summer weekday, when normal work commuters are supplemented by increased tourist traffic, as well as a seasonal peak in tanker and cargo shipping. 
- I sourced the data from AccessAIS (https://marinecadastre.gov/accessais/). I kept the dataset manageable by only selecting a 48 hour window and confining the vessel traffic data to include only the main large population centers of the Bay Area. Data filtering was undertaken via the Google Colab as well to better create a manageable dataset in 60 second intervals. 

# 2. Interpretation
- I noticed that passenger traffic in the bay area is primarily busiest during working hours, starting from around 08:00 PDT to around 19:00 PDT. I noticed particularly that traffic is busiest san-francisco bound in the mornings and vice versa in the evenings, meaning that the traffic correlates with commuter patterns of people going into the city for work in the mornings and heading back into the suburbs in the evenings. 
- Tanker vessels are usually busiest around noon, while cargo ships are pretty sporadic throughout a 24-hour window. 
- The busiest passenger corridor I noticed is between the wharf area of San Francisco and the downtown Port of Oakland, and this could best be explained by the fact that these are the two primary economic "downtowns" of the bay area, so high-density vessel traffic naturally makes sense. 
- The busiest tanker and cargo corridor I saw on the map is between the outward Pacific ocean and the Port of Oakland. This is likely because Oakland is the main recipient of international cargo traffic for the bay area. None of the tankers or cargo ships were docking in San Francisco, likely because of how urbanized San Francisco is, as well as a smaller port that is less able to handle huge containers like how Oakland can. 

# 3. Feature Proposal for a Potential User
- I think a potential visualization service would be to identify passenger traffic for the Coast Goard to see potentially where there might be high-traffic areas that can be better managed. I would imagine they would want to see specific details on passenger vessels, and the way to do that would be using the deck.gl tooltip option. 
- deck.gl article: https://deck.gl/docs/developer-guide/interactivity
- The tool could be used to find the vessel identifier on specific vessel paths and use speed information to better learn about passenger traffic, particularly high-speeders in heavy traffic areas. This tool can help to find specific violators of speeding and help the Coast Guard better patrol the bay area. 
