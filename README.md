# Install Bootstrap Content & Config

Download magnolia as normal - BUT DONT START THE SERVER.
(This process only works when the Magnolia instance runs its first install step)

Copy all files from `/magnolia/_dev/content-to-bootstrap` into
`/magnolia/apache-tomcat/webapps/magnoliaAuthor/WEB-INF/bootstrap/common`

Start magnolia
(All files in that directory will be automatically imported into magnolia)
* Most of the files are content.
* `config.modules.site.config.site.travel.xml` Imports a site definition (which declares the theme and language locales)
* `config.server.filters.addCORSHeaders.xml` Imports CORS configuration.

# Configure CORS

Log into adminCentral - we have to move the filter.
* Open Configuration app
* Find /server/filters and scroll to the end.
* Move `addCORSHeaders.xml` directly after `uriSecurity` (a few items up.)
  * You can drag-n-drop it, but take care not to drop it in a folder by accident. If you do you can just drag it back out though.

# Install content

To install sample tours content
* Open Tours app
* Click `Import` action
* Select the file `/magnolia/_dev/content-to-import/tours.magnolia-travels.xml`
