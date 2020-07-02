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

2. Click on the **Incident start** to select the start time

3. **OPTIONAL** Click on **Incident end** to selec the end time. An ongoing incident has no end time specified or you can specify an end time that is far enough in the future to likely postdate the incident.

4. Give the incident a name (e.g. 20181114 Burbank Fire)

5. Click **Create region/incident and show EmComMap** button

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

Incident Workflow
+++++++++++++++++

Once the EmComMap application has loaded, your screen should look something like this:

   .. image:: _images/emcommap_incident_mainpage.png
      :alt: EmComMap Incident Main Page
      :align: center
      
At the top shows who you are and the current incident. To change incident, click on the incident description. You may enter a tactical ID by pressing the “Change” button; you can alter it as often as needed. The left side displays a map of the incident’s region, with its rectangular border outlined in red. Locations outside this region and message traffic relevant to them are not displayed, allowing multiple unrelated incidents to be operationally segregated. If you wish to view multiple such regions simultaneously, then define a new region which contains all the regions of interest and then create a new incident based on that new region.

The map shows various locations with associated markers. Marker symbols are shown in Table 1. You may zoom into and out of the map using the + and – buttons on the upper left, and you may use the mouse to pan (some trackpad gestures will also allow zooming). Clicking on or hovering over the various markers will either transfer their information to the right-hand panel or show information as a tooltip near the pointer position.

