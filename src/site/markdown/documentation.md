<!---
Copyright (C) 2015  Karl Bennett

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
-->
## Plugins

This parent pom provides the following plugins.

### Mandatory
The following plugins will be added to all SMT projects.

#### org.apache.maven.plugins:maven-compiler-plugin
The Maven compiler plugin is used to set the compile target of all the projects to Java 7.

#### org.apache.maven.plugins:maven-release-plugin
The release plugin is added to make sure all SMT projects are using the same version.

### Optional
The following plugins and their configuration can be optionally inherited by SMT sub-projects.

#### org.apache.maven.plugins:maven-site-plugin
The Maven site plugin has been configured with Markdown support.

#### org.apache.maven.plugins:maven-project-info-reports-plugin
The Maven report plugin has been added to allow the selection of specific Maven reports.

#### org.jacoco:jacoco-maven-plugin
The Jacoc plugin has been configured to automatically generate coverage reports that will be embedded in the projects
site.

## Profiles

### github

This profile is used to deploy the generated maven

#### com.github.github:site-maven-plugin
The Github site plugin automatically copies and commits the projects site into the gh-pages branch so that it will be
hosted by Github.

### central-build

This profile is used when carrying out a build that is to be deployed into central. It contains all the plugins required
for a central deployment.

#### org.apache.maven.plugins:maven-source-plugin
All artifacts deployed to central must be accompanied with their source code.

#### org.apache.maven.plugins:maven-javadoc-plugin
All artifacts deployed to central must be accompanied with their JavaDocs.

#### org.apache.maven.plugins:maven-gpg-plugin
All artifacts deployed to central must be signed.

## Dependencies

This parent pom provides the following dependencies.

### junit:junit
JUnit is provided in the `test` scope to facilitate writing unit tests.

### org.hamcrest:hamcrest-all
The entirety of the Hamcrest library is provided in the `test` scope to allow access to all the matcher's.

### org.mockito:mockito-all
Mockito is provided in the `test` scope because when writing tests mocks are almost always necessary.