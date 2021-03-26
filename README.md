# sf_reports

sf_reports is a simple Drupal 6 module that displays the list of current organisation presidents. The list is automatically updated depending on the current date and takes data directly from the Salesforce database.

Installation
------------
Upload module into the Drupal modules directory and enable it. The module requires Salesforce API module to be enabled.

After the sf_reports module is installed, the following URL is created:

`/sfreport/presidents`
 
There are two access permissions created as well:

 1. `view presidents report - public`
    allows users to see presidents list containing:
       - first name, last name, name of the organisation, organisation email
           
 2. `view presidents report - private`
    allows users to see presidents list containing:
       - first name, last name, name of the organisation, president's email, president's mobile
 
You can assign these permissions to users at `/admin/user/permissions`.

If needed, you can create menu items pointing to the created URLs.


Emebedding presidents list into any content
-------------------------------------------

If you access the created URL with trailing "/html" like this:

  `/sfreport/presidents/html`
  
  ...then plain HTML is returned instead of themed output. You can use this
  feature to embed presidents list into any content using iframe.
  

Browsing through the whole database of presidents
-------------------------------------------------
  
When you visit `/sfreport/presidents`, the form is displayed. You can specify
start and end date of president role for database query.


Disclaimer
----------

This module is in no way affiliated with Salesforce.com, Inc. No endorsement is expressed or implied. Salesforce.com, Inc. and the Salesforce.com logo are trademarks of Salesforce.com, Inc.

Author
------
Ivan Ottinger (http://drupal.org/user/768478)
