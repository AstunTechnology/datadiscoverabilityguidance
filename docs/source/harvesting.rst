Harvesting
----------

This section outlines the options available for harvesting spatial and non-spatial metadata from various endpoints.

To set up a new harvester in GeoNetwork 4.x login as an Administrator and go to Admin console > Harvesting > Catalog harvesters

To add a new harvester click on the **Harvest from** dropdown. The available sources are:

* ArcSDE
* Directory- this will harvest from a directory located on the same server as GeoNetwork
* GeoNetwork (2.0)
* GeoNetwork (from 2.1 to 3.x)
* GeoPortal REST
* OAI/PMH
* OGC CSW 2.0.2
* OGC Web Services
* OGC WFS GetFeature
* Simple URL
* Thredds catalog
* WebDAV/WAF

|Harvester dropdown|

**Directory harvesting**

This option allows users to harvest records from the same server that runs GeoNetwork. 

.. important::
    If you are running GeoNetwork in a dockerised manner you will need to map the local directory to a volume and the path will become the mapped volume path.
    For example if the docker mapping is `./harvester-test:/var/lib/jetty/webapps/geonetwork/harvester-test` then the path that the harvester needs to be pointed at has to be `/var/lib/jetty/webapps/geonetwork/harvester-test` 

|Directory harvesting|
An example setup for harvesting in a dockerised setup

The main configuration options for a directory harvest are:
* Node name and logo- this is the name of the harvester and a logo
    * Note: in order to be able to associate a logo to the harvester, it needs to be pre-loaded into the catalog. This can be done in Admin console > Settings > Logo
* Group- the group which owns the harvested records
* User- a user can be picked from the list and will be the owner of the records
* Schedule- this feature can be enabled or disabled. If enabled, the user can set a recurring harvest
* Directory- this is the path to the Directory that holds the records
* Also search in subfolders- if ticked this will point the harvester to any existing subfolders too
* Action on UUID collision- this dictates what action will be taken if a UUID already exists in the catalog. This can be set to:
    * Skip record (default)
    * Overwrite record
    * Create new UUID
* Update catalog record only if file was updated (tickbox)
* Keep catalog record even if deleted at source (tickbox)
* Validate records before import- the default option is to accept all metadata without validation
* XSL transformation to apply
* Batch edits
* Category- the category to be allocated to the harvested records
* Group privileges for the harvested records


.. |Harvester dropdown| image:: media/harvesterdropdown.png
    :alt: Dropdown menu showing the available harvesting options in GeoNetwork 4.x
.. |Directory harvesting| image:: media/directoryharvesting.png