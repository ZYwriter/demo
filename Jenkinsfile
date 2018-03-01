pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''../../tools/node_modules/karma/bin/karma start /var/lib/jenkins/tools/karma.conf.js 

rm -rf Mozilla

rm -rf coverage

cp -r /var/lib/jenkins/tools/Mozilla .

cp -r /var/lib/jenkins/tools/coverage .
'''
      }
    }
    stage('Test') {
      steps {
        echo 'Hello'
      }
    }
  }
}