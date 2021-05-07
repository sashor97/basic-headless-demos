# Install Bootstrap Content & Config

Download magnolia as normal - BUT DONT START THE SERVER.
(This process only works when the Magnolia instance runs its first install step)

Copy all files from `/magnolia/_dev/content-to-bootstrap` into
`/magnolia/apache-tomcat/webapps/magnoliaAuthor/WEB-INF/bootstrap/common`

Start magnolia
(All files in that directory will be automatically imported into magnolia)
* The files are sample content.

# Install content

To install sample tours content
* Open Tours app
* Click `Import` action
* Select the file `/magnolia/_dev/content-to-import/tours.magnolia-travels.xml`

# Run the frontend

Open up the `frontend\index.html` file in any web browser, for example by double clicking on it.

## Permissions for Images

What? No images displaying? We need to allow anonymous access to the image urls since we are running on the author instance.

* Open the [Security app](http://localhost:8080/magnoliaAuthor/.magnolia/admincentral#app:security:roles;/anonymous:treeview:), open the `Roles` tab, and edit the `anonymous` role. 
* Go to `Web access` tab, click `Add new`and enter path `/.imaging*` set to GET.

