Requirements
============

.. IMPORTANT::
	To follow this guidance you will need to have an installation of GeoNetwork Open Source, with version 4.2.x. Some functionality worked differently in previous versions.

For instructions on installing GeoNetwork, and guidance on getting started, please see the `official documentation <https://www.geonetwork-opensource.org/manuals/4.0.x/en/install-guide/index.html>`__.

You will also need to install the plugins for `Gemini 2.3  <https://github.com/AstunTechnology/iso19139.gemini23>`__ (for spatial data), and `iso19139.nonspatial <https://github.com/AstunTechnology/iso19139.nonspatial>`__ (for non-spatial data).

Once you've restarted GeoNetwork, you can check that the metadata profiles have loaded correctly by logging in as an Administrator and going to the Admin console > **Metadata and templates** page. 

The list should include the following additional entries (alongside the pre-loaded ones):

* Non-spatial metadata profile based on iso19139 (iso19139.nonspatial)
* iso19139.gemini23 (iso19139.gemini23)

|configuration_metadataandtemplates|

Click the dropdown box on the right marked **0 selected** and choose **All**, then click the buttons below the templates list to **Load templates for selected standards** and **Load samples for selected standards**.
This will load all the available templates and sample records into your catalog.

.. |configuration_metadataandtemplates| image:: media/configuration_metadataandtemplates.png
