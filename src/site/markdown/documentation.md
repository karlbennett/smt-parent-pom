This parent pom provides te following plugins.

### org.apache.maven.plugins:maven-source-plugin
The Maven source plugin is present to make sure that the projects source is deployed.

### org.apache.maven.plugins:maven-site-plugin
The Maven site plugin has been configured with Markdown support.

### org.apache.maven.plugins:maven-project-info-reports-plugin
The Maven report plugin has been added to allow the selection of specific Maven reports, at the moment this is just the
SCM (Source Control) report.

### org.apache.maven.plugins:maven-release-plugin
The release plugin is used for release all SMT projects, it is best practice to lock the version of this plugin.

### org.apache.maven.plugins:maven-javadoc-plugin
The Maven JavaDoc plugin causes JavaDocs to be generated.

### org.jacoco:jacoco-maven-plugin
The Jacoc plugin has been configured to automatically generate coverage reports that will be embedded in the projects
site.

### com.github.github:site-maven-plugin
The Github site plugin automatically copies and commits the projects site into the gh-pages branch so that it will be
hosted by Github.