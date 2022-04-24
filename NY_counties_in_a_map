library(tidyverse)
library(ggplot2)
library(dplyr)
library(countrycode)
library(maps)
library(ggmap)
library(mapdata)
library(ggthemes)
install.packages("ggh4x")
library(ggh4x)

states <- map_data("state")
View(states)

ggplot(data = states) + 
  geom_polygon(aes(x = long, y = lat, fill = region, group = group), color = "white") + 
  coord_fixed(1.3) +
  guides(fill=FALSE)  # do this to leave off the color legend

ny_df <- subset(states, region == "new york")
View(ny_df)

counties <- map_data("county")
View(counties)

ny_county <- subset(counties, region == "new york")

View(ny_county)

ggplot(data = ny_county, mapping = aes(x = long, y = lat, group = group, fill = subregion)) + 
  geom_polygon(color = "red", show.legend = FALSE)+
  labs(title= "NY State Counties", caption = "Week 5 R Practice")+
  theme(legend.position="left")+
  coord_quickmap()+
  stat_midpoint(aes(label = subregion), geom = "text",size=3) +
  coord_map()
  





