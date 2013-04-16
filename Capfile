load 'deploy'

set :application, "jujuca"
set :deploy_to, "/www/jujuca"
set :deploy_via, :copy
set :repository, "build"
set :scm, :none
set :copy_compression, :gzip
set :use_sudo, false
set :domain, 'jujuca.com'
set :user, 'deploy'

role :web, domain

before 'deploy:update_code' do
  run_locally 'middleman build -c'
end