---
layout: post
title: Drones over Canaan, Haiti
postID: canaan-drones
category: blog
banner:
date: 2018-01-18
author: Matthew Gibb and Dan Joseph
excerpt:  In what has become the second largest populated area in Haiti, Canaan continues to evolve and grow. The American Red Cross recently covered 35 square kilometers of this area with new drone imagery to assist with population estimates, disaster preparedness programming, and for updating OpenStreetMap.
Published: false
tags: [Haiti, Canaan, drones, OpenDroneMap]
permalink: /blog/:year/:month/:day/:title/
lang: en
---

(EMBED VIDEO OF CANAAN APPROACH?)

Eight years after the devastating earthquake in January 2010, the landscape in Haiti is continuously changing. For organizations working in Haiti, recovery programs slowly transitions to preparedness and disaster risk reduction. More importantly, for over 250,000 people north of Port-au-Prince a blank slate, a patch of land, transitions into a future. The resourcefulness of this community has been [well documented](http://www.redcross.org/news/article/In-Canaan-Haiti-residents-guide-the-citys-development). Since 2014, the American Red Cross has been supporting residents of this community through [health, infrastructure, and livelihoods programs](http://www.redcross.org/news/article/Haiti-Canaan-residents-join-together-to-overcome-economic-challenges).
Canaan has grown so rapidly, that keeping a map of the area up to date is extremely difficult, and some communities within the area are becoming so dense that satellite imagery is becoming more difficult to interpret. To provide new imagery for the community and partner organizations working there, the American Red Cross has collected, processed, and made available imagery for the entire 35 square kilometer area.

# Equipment

Canaan lies in rolling foothills about 10km north of Port-au-Prince. The growing population has led to dense urban areas in central areas, and more sparsely populated areas in further less developed areas (although as seen by the amount of construction, this is rapidly changing). To account for this, we utilized DJI’s Mavic Pro quadcopter. Depending on weather conditions, the Mavic Pro gets around 25 minutes of flight time, and through the use of the DroneDeploy app, flights are easy to plan and continue when batteries need to be changed out.

Given the Mavic Pro’s size and sensor capabilities, it takes more flights and many more pictures than a fixed wing drone to cover the large areas needed for this mission, To account for this, we included 20 batteries and utilized power converters that could charge batteries in our vehicle while flights continued.

To improve accuracy of our orthomosaic, at each launch point, ground control points (GCPs) were used. (DAN TO ADD SOMETHING HERE)

<figure>
<img src="https://arcmaps.s3.amazonaws.com/share/blog-pictures/canaan-drones_GCP-placed.jpg">
<p class="caption">Ground control point placed near launch site, CC-BY American Red Cross</p>
</figure>

Ideally for an area as large as Canaan, we would be able to use a fixed wing drone, which has a slightly longer battery life, a camera sensor with a wider angle allowing for more area to be covered by a single picture. We’ve used a platform called the Tuffwing UAV Mapper. Unfortunately, due to factors like excessive wind and the need for a large landing area, using the Tuffwing for our mission in Canaan was not feasible. We were able to fly the Tuffwing to capture imagery for one neighborhood, and the quality benefits of the platform were immediately seen.

(COMPARISON PICTURE OF TUFF WING VS MAVIC IMAGERY?)

# Flight Planning

_The best laid plans of mice and men, go oft awry_ - Robert Burns, paraphrased

It’s easy to set up what appears to be a flawless plan 1,400 miles away, but regardless, failing to plan is planning to fail. With what we knew of the Canaan area and the capabilities of the Mavic Pro drones, we created a grid of 1km squares to guide our flight plans and make our itinerary. Much of this however went out the window upon arrival in Port-au-Prince.

When using drones in humanitarian contexts, one of the most important aspects of planning is community sensitization and buy-in. With the American Red Cross presence in Canaan, there is a fantastic network of community focal points. These are community members from each neighborhood in Canaan, who work with community leaders and members to help provide context for each neighborhood, as well as provide a way to communicate effectively regarding project related topics within the neighborhood. Community mobilizers from the American Red Cross worked with these focal points to explain ahead of time, the goal of the project and to address any concerns ahead of time. More information about best practices when using drones in humanitarian contexts can be found on the [UAviators website](https://humanitariandronecode.wordpress.com).

In some neighborhoods, these conversations were completed faster than others. Because of this, our initial itinerary changed very quickly.

Once we had a better idea of the timeline for which we would be able to fly over certain communities, we worked out a more efficient plan for selecting flight locations. Using our initial grid as guidance, we used an ASTER DEM to identify centrally located high points in the landscape. Using these points, we calculated Voronoi Polygons to have a better idea of reachable areas from a given launch point. We would then edit these polygons to create more "reasonable" (totally subjective) areas for a given flight. We didn't want too many very small areas, as travel time would ultimately take away from flying time. We preferred to send the drone a bit further rather than pack up, travel, and unpack to do a short flight. Ultimately we made judgement calls based on the topography. We created overlap with neighboring flight areas as well as areas between assigned days. The overlap would ensure coverage of a given location in case the direction of the flights varied slightly.

The polygons of the flight areas were converted to `.kml` files and uploaded to the DroneDeploy website. Most flight altitudes were set to 160 meters with 70% side-lap and 80% front-lap. With no UAS regulation in Haiti (rumored to change in February), little air traffic, and very clear lines of sight, we were able to fly at this altitude consistently throughout our mission. After selecting the flight direction (which could be edited upon arrival at the flight location to adjust for wind or obstacles), the flight plans could then be synced to the DroneDeploy iPad app, which connects to the Mavic Pro flight controller and is used to program the drone for its flight.

# Flying

Using the pre-identified launch points, they were converted to a `.gpx` waypoint. These were then added to the OSMand mobile app, and given the road network already traced into OSM, used to navigate to the point. Depending on the neighborhood that we would be flying in that day, we would travel with the community focal point for that neighborhood. The community focal point would work with us to explain to and demonstrate for onlooking community members, the work that we were doing with the drones.

Depending on the layout of the area upon arrival, we could adjust the flight angles and fly 2 Mavic Pros concurrently to cover the area. Especially on days with high wind, this method worked well in making sure the entire area was covered.

In addition to flights, we used two Sony Action Cameras to capture street level imagery as we drove throughout Canaan. The imagery of the area can be viewed on [Mapillary](https://www.mapillary.com/app/?lat=18.652149722222248&lng=-72.29545138888886&z=17&pKey=qesHt-3rIoVgYZaYtguNsQ&focus=photo) and [OpenStreetCam](http://openstreetcam.com/details/990741/207). Both forward facing and side facing images were captured.

<figure>
<img src="https://arcmaps.s3.amazonaws.com/share/blog-pictures/canaan-drones_mapillary.jpg">
<p class="caption">Camera collecting street level imagery for Mapillary and OpenStreetCam, CC-BY American Red Cross</p>
</figure>

<iframe width="640" height="320" src="https://embed-v1.mapillary.com/embed?version=1&filter=%5B%22all%22%5D&map_filter=%5B%22all%22%5D&map_style=mapbox_streets&image_key=qesHt-3rIoVgYZaYtguNsQ&x=0.5&y=0.5&client_id=MFpjMU5abGRUMmxoQjEzdUNUMFRjdzo3NmEwODNjYzdkNGQ5OWE5&style=split" frameborder="0"></iframe>

Over 6 flying days (with excessive wind having grounded us for 2 days), a total of XXXXX flights were flown. A total of 28,232 nadir facing images from the Mavics (over 120 GB) and 133,109 street level images were collected.

# Processing

At the American Red Cross, we support the use of open source software, and have contributed to the OpenDroneMap project. Due to the magnitude of images that were collected, we processed the images in 66 separate groups, each less 1000 images, making sure that there was significant overlap of these areas for continuity of processing. This process took ONE MILLION HOURS

(PICTURE OF PROCESSING AREAS)

Following the processing, the scenes were merged using GDAL. Once the merged orthomosaic was complete, we georeferenced the mosaic using the ground control points that were laid out at each launch site.

(PICTURE OF GCP FROM DRONE)

The orthomosaic has been added to OpenAerialMap. New mapping projects have been created on the HOT Tasking manager. Due to the density of the area and presence of existing data, these projects are available to advanced mappers only.

The imagery has been shared with American Red Cross staff as well as partners and organizations working in Canaan to improve population estimates, plan DRR activities, and assist with community planning.
