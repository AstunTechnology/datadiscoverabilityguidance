Configuration
=============

You will need to change a number of settings in the administrator panel to get best use out of GeoNetwork. Login in as an administrator, and visit Admin Console -> Settings.

In the main **System Settings** tab, we recommend making changes to the following sections. Note that there are many other options that you can also change, see `the official documentation <https://www.geonetwork-opensource.org/manuals/trunk/en/administrator-guide/configuring-the-catalog/index.html>`__ for more information:

**Catalog Description**

* Fill in a Catalog Name
* Fill in the Organization

**Catalog Server**

* Change the **Host**, **Preferred Protocol**, **Port** and **Secure Port** to match your install. For example if you access the catalog at the URL https://mygeonetwork.com/geonetwork then you'd set the following:
  * Host: mygeonetwork.com
  * Preferred Protocol: https
  * Port: blank
  * Secure Port: blank
 
* For the **Timezone**, set the most appropriate one for you. In the UK this is probably *Europe/London*

**Feedback**

* Change the **Email** to the address you want catalog emails to come **from**
* Fill in the address of your mailserver (the **SMTP host**, and set the rest of the options in this section as appropriate.

 To test, save your changes and then click the **Test mail configuration** button. This will send an email **to** the specified address, so make sure it's one you have access to.

.. WARNING::
 	If the catalog server is not part of the same domain as the email address, then messages from GeoNetwork may be classified as spam.

 
**User feedback**

* Click the **Enable feedback** option to allow people to leave comments on records

**Search statistics**

* Click the **Enable** option to store search statistics

**INSPIRE Directive configuration**

* Click the **INSPIRE** option to enable the ability to display records by INSPIRE theme on the home page. Ensure you have the INSPIRE thesaurus installed (see `the page on classification systems <classificationsystems.html>`__ for details)
* Click the **INSPIRE search panel** option.

**Metadata configuration**

* Click the **Remove schema location for validation** option. This prevents validation errors from records where the schemalocation is incorrect or cannot be reached. In this case the schema files loaded on your local server are used instead.

.. important::
	Be sure to click the blue **Save Settings** button to save your changes!