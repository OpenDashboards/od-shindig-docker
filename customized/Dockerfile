##################################################################
# OpenDashboards - Shindig - Docker - Customized server
#
# Description
# -----------
# Extends the basic Shindig image and adds custom configuration
#
# Author: Chris Spiliotopoulos (@chefArchitect)
##################################################################

# Extend the bootstrap Shindig image
FROM opendashboards/od-shindig-docker:bootstrap

MAINTAINER Chris Spiliotopoulos (@chefArchitect)

ADD shindig.properties webapps/ROOT/WEB-INF/classes/shindig.properties
ADD containers webapps/ROOT/WEB-INF/classes/containers

#
# Launch the Jetty engine
#

CMD java -Djava.io.tmpdir=/tmp/jetty -Dshindig.host=$SHINDIG_HOST -Dshindig.port=$SHINDIG_PORT -jar /usr/local/jetty/start.jar jetty.port=$SHINDIG_PORT
