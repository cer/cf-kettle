require "fileutils"

root = File.expand_path("..", __FILE__)

desc "install all gem dependencies"
task :bundle_install do
  bundle_cmd = "bundle install"

  %w(vcap-common vcap-staging stager nats dea cloud_controller/cloud_controller .).each do |component|
    sh "cd #{component} && #{bundle_cmd}"
  end

  %w(cloud_controller/cloud_controller).each do |component|
  	sh "cd #{component} && rake db:migrate"
  end
end
