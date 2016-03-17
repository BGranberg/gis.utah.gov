---
layout: post
status: publish
published: true
title: How To Use AGRC Base Maps in QGIS
author:
  display_name: Scott Davis
  login: Scott Davis
  email: stdavis@utah.gov
  url: ''
author_login: Scott Davis
author_email: stdavis@utah.gov
wordpress_id: 16332
wordpress_url: http://gis.utah.gov/?p=16332
date: '2015-01-20 07:51:04 -0700'
date_gmt: '2015-01-20 14:51:04 -0700'
categories:
- Uncategorized
- Developer
tags:
- mapping
- arcgis
- open source
- base maps
---
<p>Most people know about AGRC&#39;s awesome <a href="{{ "/data/sgid-base-map-services-arcmap/" | prepend: site.baseurl }}">base maps</a>. They are <a href="{{ "/basemaps-a-2014-day-in-the-life/" | prepend: site.baseurl }}">very popular</a> and provide high quality cartography using the latest and greatest data from the <a href="{{ "/data/" | prepend: site.baseurl }}">Utah SGID</a>. But did you know that they provide a <a href="http://en.wikipedia.org/wiki/Web_Map_Tile_Service">WMTS</a> service that can be consumed in non-ESRI products?</p>
<p>Here&#39;s how to load our base maps in <a href="http://www.qgis.org/en/site/">QGIS 2.6.1</a>:</p>
<ol>
<li>The first step is to find the URL to the service that you are interested in. Most of AGRC&#39;s base maps are within a folder called &quot;<a href="http://mapserv.utah.gov/arcgis/rest/services/BaseMaps">BaseMaps</a>&quot; on our main ArcGIS Server instance. Once you find the specific layer that you are interested in, copy the URL for the WMTS link at the top of the services directory page:<br><img src="http://i.imgur.com/4lXjFFl.jpg" alt="link" width='760'></li>
<li>Open QGIS and click on the &quot;Add WMS/WMST Layer&quot; button to open the &quot;Add Layer(s) from a WM(T)S Server&quot;.</li>
<li>Click on the &quot;New&quot; button to open the &quot;Create a new WCS connection&quot; dialog and add a name for the layer and the URL to the WMTS service and click &quot;OK&quot; to close the dialog.<br><img src="http://i.imgur.com/zwN1Uag.jpg" alt="dialog" width='760'></li>
<li>You should now see a new layer in the add layer dialog. Select the new layer and click on the &quot;Add&quot; button to add it to the map.<br><img src="http://i.imgur.com/ZHvujIc.jpg" alt="dialog" width='760'></li>
<li>You should now be able to view the base map as a layer in QGIS!<br><img src="http://i.imgur.com/di10u7z.jpg" alt="map" width='760'></li>
</ol>
<h2 id="bonus-tip">Bonus Tip</h2>
<p>If you are having performance issues using our cached services through ArcMap, try loading them via these WMTS services. You can do this by double-clicking on the &quot;Add WMTS Server&quot; node in the ArcCatalog tree under &quot;GIS Servers&quot; and then pasting the same URL as above.<br />
<img src="http://i.imgur.com/ydArdcM.jpg" alt="arcmap"></p>