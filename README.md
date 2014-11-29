# Docker Overviewer

This dockerfile creates a [Minecraft Overviewer](overviewer.org) container  to
generate minecraft maps from a minecraft world.

1. Edit the `overviewer.cfg` file to point to your world files and set the output directory and other options.
2. Start the container:
    - `# docker run -d -v /vagrant/overviewer-data/world:/overviewer/world -v /vagrant/overviewer-data/maps/:/overviewer/maps --name="overviewer" overviewer:latest`
    - You need to copy or supply your world directory to the location specified above `/vagrant/overviewer-data/world`
    - Your map will be exported to the second directory, `/overviewer/maps`

**NOTE**

The container defaults to version 1.8, but using the `-e` environment flag you can specifiy which version of minecraft your world was created from:
`docker run -d -v /vagrant/overviewer-data:/overviewer/world -v /vagrant/overviewer-data/maps/:/overviewer/maps -e "MCVERSION=1.8.1" --name="overviewer" overviewer:latest`

There is no need to copy the texture files locally, since the container
automatically downloads the version you specified if it is different from the 
default version.

