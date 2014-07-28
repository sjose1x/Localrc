Localrc
=======

My Localrcfile
DEST=/opt/stack

# Logging
LOGFILE=$DEST/logs/stack.sh.log
VERBOSE=True
LOG_COLOR=False
SCREEN_LOGDIR=$DEST/logs/screen

# Credentials
ADMIN_PASSWORD=openstack
MYSQL_PASSWORD=openstack
RABBIT_PASSWORD=openstack
SERVICE_PASSWORD=openstack
SERVICE_TOKEN=tokentoken

# Github's Branch
GLANCE_BRANCH=stable/icehouse
HORIZON_BRANCH=stable/icehouse
KEYSTONE_BRANCH=stable/icehouse
NOVA_BRANCH=stable/icehouse
NEUTRON_BRANCH=stable/icehouse
HEAT_BRANCH=stable/icehouse
CEILOMETER_BRANCH=stable/icehouse

# Neutron - Networking Service
DISABLED_SERVICES=n-net
ENABLED_SERVICES+=,q-svc,q-agt,q-dhcp,q-l3,q-meta,q-metering,neutron

# Neutron - Load Balancing
ENABLED_SERVICES+=,q-lbaas

# Heat - Orchestration Service
ENABLED_SERVICES+=,heat,h-api,h-api-cfn,h-api-cw,h-eng
HEAT_STANDALONE=True

# Ceilometer - Metering Service (metering + alarming)
ENABLED_SERVICES+=,ceilometer-acompute,ceilometer-acentral,ceilometer-collector,ceilometer-api
ENABLED_SERVICES+=,ceilometer-alarm-notify,ceilometer-alarm-eval
