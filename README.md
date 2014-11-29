# Docker Overviewer

This dockerfile creates a [Minecraft Overviewer](overviewer.org) to
generate minecraft maps from a minecraft world.

1. Edit the `overviewer.cfg` file to point to you world files and set the output directory and other options.
2. Start the container:
  - docker run -d -v /vagrant/overviewer-data:/overviewer/world -v /vagrant/overviewer-data/maps/:/overviewer/maps --name="overviewer" overviewer:latest`

***More to come***

