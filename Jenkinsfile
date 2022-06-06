node {
    stage ('Clone') {
      checkout scm 'https://github.com/justalever/demo_blog_rails.git'
    }
    stage ('Build') {
        sh gem install bundler
        sh bundle install
        sh 'cp config/database-gitlab.yml config/database.yml'
        sh 'bundle exec rake db:create db:migrate RAILS_ENV=test'
        sh 'bundle exec rake test'
        
    }
    stage ('Tests') {

    }

}
