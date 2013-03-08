nats: env BUNDLE_GEMFILE=./nats/Gemfile ./nats/bin/nats-server
dea: env BUNDLE_GEMFILE=./dea/Gemfile ./dea/bin/dea -c config/dea/dea-laptop.yml
stager: env BUNDLE_GEMFILE=./stager/Gemfile ./stager/bin/stager -c config/stager/stager.yml
cloud_controller: sh -c 'cd cloud_controller/cloud_controller && env CLOUD_CONTROLLER_CONFIG=../../config/cloud_controller/cc_config.yml bin/cloud_controller'