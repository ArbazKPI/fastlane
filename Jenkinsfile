#! groovy

pipeline {
    agent any

    stages{

    stage('Setup') {
  steps {
    echo "Setup"

    sh sudo -i
    // Install bundler in order to use fastlane
    sh "gem install bundler"
    // set the local path for bundles in vendor/bundle
    sh "bundle config set --local path 'vendor/bundle'"
    
    sh "bundle install"

    sh "bundle exec fastlane beta"
  }
}
}
}