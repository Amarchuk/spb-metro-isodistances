# Saint-Petersburg Metro Isodistances

[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/Amarchuk/spb-metro-isodistances)

**About:** It is a one-day project in which I try to plot maps of equal distance to Saint-Petersburg subway ('metro') stations, also called isodistances. I try to achive this with the help of public APIs and Jupyter Notebook.

[View notebook on Nbviewer](http://nbviewer.ipython.org/github/Amarchuk/spb-metro-isodistances/blob/master/Metro%20Isodistances.ipynb)

**New technologies**: get taste of standart python package for maplike-work [basemap](http://matplotlib.org/basemap/users/index.html), work with [Yandex Geocoder](https://tech.yandex.ru/maps/geocoder/) and [Open Source Routing Machine: The OpenStreetMap Data Routing Engine](https://github.com/Project-OSRM/osrm-backend/wiki/Server-api)

**How:** first of all, I get static map of SPb and use Geocoder to get longitude and latitude by station name. Then for 100x100 grid we find nearest stations and measure distances to them from grid points in two different ways. I measure distance both on earth surface and real travel distances with the 'table request' in OSRM service anf then plot data on map.

**Troubles:** 
1. Google and Yandex use Javascript in their route APIs. All what I do may be perfectly done in easier way using such interface calls, but I din't know JS adequately
2. Yandex uses uncommon projection in his map and it is difficult to plot it in basemap
3. working with basemap was confusing (I better try [folium](https://github.com/python-visualization/folium) next time!)
4. OSRM responce in table request restricted by 100х100 points, gather all data take some time

**Results:** 

![direct isodistances](https://raw.githubusercontent.com/Amarchuk/spb-metro-isodistances/master/direct_isodist.png "direct isodistances")

![OSM isodistances](https://raw.githubusercontent.com/Amarchuk/spb-metro-isodistances/master/OSM_isodist.png "OSM isodistances")
