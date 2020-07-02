==================
EmComMap Operation
==================

EmComMap is currently served on multiple servers on the AREDN mesh network. List of current stable servers are listed here.

EmComMap has been tested on Chrome, Firefox, Safari and the new Microsoft Edge browers.

Accessing & Logging In
----------------------

   .. image:: _images/emcommap_login_screen.png
      :alt: EmComMap Login Screen
      :align: right

1. Open your web broswer and go to **http://<address or IP>:8080/** 

2. Enter your username and password.

3. Select your desired database and map tile servers. Unless you have access to a different host database and map tile server, use the default database host in **Remote host** and **Tile server URL**.

4. Click **Login**

|
|
|
|
|
|

.. note:: You may be able to log in as **guest** with password **guest**. If you would like personal credentials, contact the host administrator.

.. note:: If you have difficulty logging in, take note of any error messages that appear on the javascript console within your browser and forward to the app developers emcommap@gmail.com.

.. note:: Alternatively to working in a multi-operator environment, you can operate in standalone/single user mode by clicking the **Standalone mode** radio button. This will work only with data that is local to your browser and not shared with others, so it’s a good way to either experiment or to scribe traffic for a voice net.

.. warning:: When using **Standalone mode**, be very careful not to clear your browser cache, or you will lose all your data!

Incident Management
-------------------

Once logged in, you will be able to choose and existing incident or create one of your own.

   .. image:: _images/emcommap_incident_select.png
      :alt: EmComMap Incident Select
      :align: center

Open Existing Incident
++++++++++++++++++++++

1. Click on the dropdown labeled **select an existing incident** and choose your desired incident.

2. Click **Show EmComMap** button to open the incident.

.. note:: If the selection box entitled **Select existing incident** does not contain any incidents, you may need to wait a few seconds for the database to sync or try refreshing the page. If it stays empty, then there may be no incidents yet defined, so that you will need to define one.

Create a New Incident
+++++++++++++++++++++

To create a new incident, use the **Define new incident** area.

Select an existing region if applicable or define a new region on the map.

Existing Region
"""""""""""""""

1. Click the **Select existing region** dropdown and choose an existing region

   .. image:: _images/emcommap_incident_startdate.png
      :alt: EmComMap Incident Start Date
      :align: right

2. Click on the **Incident start** to select the start time

|
|
|
|
|
|
|
|
|
|
|
|

   .. image:: _images/emcommap_incident_enddate.png
      :alt: EmComMap Incident End Date
      :align: right
      
3. **OPTIONAL** Click on **Incident end** to selec the end time. An ongoing incident has no end time specified or you can specify an end time that is far enough in the future to likely postdate the incident.

|
|
|
|
|
|

4. Give the incident a name (e.g. 20181114 Burbank Fire)

5. Click **Create region/incident and show EmComMap** button.

New Region
""""""""""

1. Scroll down to the map area and click the box with the filled black square on the left

2. Drag a rectangle on the map.

.. note:: If you wish to edit the rectangle once created, press the button that has the pen in the unfilled rectangle. If you wish to delete the rectangle, click the trashcan button when the rectangle is selected.

3. Give the region a name in the **New region name** field

   .. image:: _images/emcommap_incident_startdate.png
      :alt: EmComMap Incident Start Date
      :align: right

4. Click on the **Incident start** to select the start time

|
|
|
|
|
|
|
|
|
|
|
|

   .. image:: _images/emcommap_incident_enddate.png
      :alt: EmComMap Incident End Date
      :align: right
      
5. **OPTIONAL** Click on **Incident end** to selec the end time. An ongoing incident has no end time specified or you can specify an end time that is far enough in the future to likely postdate the incident.

|
|
|
|
|
|

6. Give the incident a name (e.g. 20181114 Burbank Fire)

7. Click **Create region/incident and show EmComMap** button.  The new region will be defined in the database along with the new incident.

Incident Overview
+++++++++++++++++

Once the EmComMap application has loaded, your screen should look something like this:

   .. image:: _images/emcommap_incident_mainpage.png
      :alt: EmComMap Incident Main Page
      :align: center
      
At the top shows who you are and the current incident. To change incident, click on the incident description. You may enter a **Tactical ID** by pressing the **Change** button. You may alter it at anytime.

The left side displays a map of the incident’s region outlined in red. Locations outside this region and message traffic relevant to them are not displayed, allowing multiple unrelated incidents to be operationally segregated. If you wish to view multiple such regions simultaneously, then define a new region which contains all the regions of interest and then create a new incident based on that new region.

   .. image:: _images/emcommap_incident_table1.png
      :alt: EmComMap Incident Icon Table
      :align: right

The map shows various locations with associated markers. Marker symbols are shown in **Table 1**. You may zoom into and out of the map using the **PLUS** and **MINUS** buttons on the upper left corner of the map. You may also use the mouse to pan (some trackpad gestures will also allow zooming). Clicking on or hovering over the various markers will either transfer their information to the right-hand panel or show information as a tooltip near the pointer position.

On the right-hand side, there are four tabbed panes, **Traffic**, **Operators**, **Locations**, and **Incident**. In the figure above, the **Traffic** pane is displayed. You can see existing traffic in the table, with the text color coded by message precedence (green = ROUTINE, yellow = PRIORITY, red = EMERGENCY). You may send traffic of your own using the box at the bottom, which contains the Submit traffic button. If sending emergency traffic, you will be prompted to confirm prior to sending.

Below is an example of message information filled out prior to pressing the submit button:

   .. image:: _images/emcommap_incident_traffic.png
      :alt: EmComMap Incident Traffic
      :align: center

This message is being sent to the attention of **kk6da**, though everyone can view it (like sending voice traffic by radio). If you intend traffic for all operators, then leave the **To** field blank. The **Related location** is used to specify the label of a location about which the traffic is related. Once you press the **Submit traffic** button, the traffic should be displayed in the table above. This is the basic method for sending and receiving traffic.

.. note:: To prevent capitalization issues in comparisons, operator identifiers (i.e. callsigns and tactical calls) are converted to lower case. Location labels, though, are not converted; they are typically in upper case (e.g. CHH).

Interacting with the Map
++++++++++++++++++++++++

The map can be panned and zoomed. Various markers are shown on the map corresponding to locations (e.g. hospitals, police, fire, operators). Some markers will display tooltip information when hovered over with the pointer. Others perform actions when clicked. For example, when you click on a location, that location’s coordinates and label are placed within various fields in the right-hand information area. Clicking on a location also selects that location for viewing only its traffic (if the location lock is unlocked to allow it). By copying information, the application attempts to discourage the typing in of callsigns and labels to prevent errors.

In the upper right corner of the map is an icon for manipulating layers. Clicking on it allows you to toggle the appearance of markers for different types of locations. This also toggles the appearance of message traffic corresponding to those locations in the traffic table (see below). Removing locations and traffic not relevant to a particular operator helps reduce visual clutter and distractions from extraneous traffic. Below is an example of a map region with the fire markers present (left) and removed (right), also showing the map layer selector tool.

   .. image:: _images/emcommap_incident_maplegend.png
      :alt: EmComMap Incident Map Legend
      :align: right

.. note:: The map coverage is limited to the area covered by the map tile server. For instance, if the map tile server only has the map tiles for Montana loaded, then the coverage area will be limited to Montana and just a little outside the borders as seen in the image. Check with the host of the map tile server for details on server coverage.

