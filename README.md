# API-Homework
 Weather and Vacation API learning exercise, Due 1/9/21

# Observations
1) In general, in January 2021, the further north you go, the colder it gets, which makes sense because we in the Northern Hemisphere are in the dead of winter, while the Southern hemisphere in in peak summer.  

However there are exceptions caused by factors like:
    
    Altitude
    
    Ocean Currents
    
    Location: 
    
       in center of a land mass 
       
       or near the coast
    
    Going too far south where summers are not warm   
    

2) There doesn't seem to be any relationship between latitude and cloudiness.  It is interesting to note that more-than-expected readings are either 100% cloudy or 100% sunny.  I'm not sure if this is accurate data, or lazy observations by humans (or automatic weather station algorythmns?).


3) Coastal cities are heavily overrepresented, especially in the Southern Hemisphere, which has significantly more water area than land area.  By randomly generating Lat/Longs, we got many points that were in the middle of the ocean, potentially hundreds, or even thousands of miles away from the city they mapped to.  As a result, cities on the coast, and especially cities on a peninsula are significanlty over-sampled compared to cites in the interior of continents.

A potential fix to this problem is discarding any city that is more than 50 miles from it's random Lat/Long, and generating Lat/Longs until the 500+ cities are created.

