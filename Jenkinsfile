pipeline {
    agent any

      stages {
          stage('build') {
              steps {
                  echo 'building the software'
                  //sh 'npm install'
                  npm update
              }
          }
          stage('test') {
              steps {
                  echo 'testing the software'
                  sh 'npm test'
              }
          }
    }
}
