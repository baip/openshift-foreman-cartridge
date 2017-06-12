# Openshift Foreman Cartridge

This cartridge for OpenShift allows you to configure and use [Foreman](https://github.com/ddollar/foreman) to run processes in the background. [Adapted](https://github.com/ncdc/openshift-foreman-cartridge) to work with Ruby 2.4 or 2.3 [here](https://github.com/baip/openshift-ruby-cartridge).

# Installation
Once you have an existing OpenShift application, run the following command:

    rhc cartridge add -a app_name http://cartreflect-claytondev.rhcloud.com/reflect?github=baip/openshift-foreman-cartridge

# Usage
In the root of your application's git repository, create a file called Procfile. Then add one or more entries such as:

    mytask: bundle exec rake resque:work QUEUE=*

# Logging
Output from Foreman is written to $OPENSHIFT_LOG_DIR/foreman.log

# Limitations
This cartridge does not currently listen on any ports.

# License
Licensed under the Apache Software License, v2.0. Please see LICENSE for more information.
