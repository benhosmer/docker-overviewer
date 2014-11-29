# Docker Overviewer

This dockerfile creates a [Minecraft Overviewer](overviewer.org) to
generate minecraft maps from a minecraft world.

1. Edit the `overviewer.cfg` file to point to you world files and set the output directory and other options.
2. Start the container:
  - docker run -d -v /vagrant/overviewer-data:/overviewer/world -v /vagrant/overviewer-data/maps/:/overviewer/maps --name="overviewer" overviewer:latest`

**NOTE**
The container defaults to version 1.8, but using the `-e` environment flag you can specifiy which version of minecraft your world was created from:
`docker run -d -v /vagrant/overviewer-data:/overviewer/world -v /vagrant/overviewer-data/maps/:/overviewer/maps -e "MCVERSION=1.8.1" --name="overviewer" overviewer:latest`

