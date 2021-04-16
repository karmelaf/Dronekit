# import the library
import folium

# Make an empty map
m = folium.Map(location=[20,0], tiles="OpenStreetMap", zoom_start=2)

# Import the pandas library
import pandas as pd

# Make a data frame with dots to show on the map    value is radius of circle --> long & lat and value should be coded right into
data = pd.DataFrame({
   'lon':[-118],
   'lat':[35],
   'name':['Forest Fire Area'],
   'value':[10] 
}, dtype=str)

# add marker on map (if we want to widen circle not to be on sensors multiple value by #)

for i in range(0,len(data)):
   folium.Circle(
      location=[data.iloc[i]['lat'], data.iloc[i]['lon']],
      popup=data.iloc[i]['name'],
      radius=float(data.iloc[i]['value']),
      color='crimson',
      fill=True,
      fill_color='crimson'
   ).add_to(m)

# Show the map again
m
