pipeline {
    agent any

      stages {
          stage('build') {
              steps {
                  echo 'building the software'
                  //sh 'npm install'
                  //sh 'npm update'
                    sh 'npm install $(npm outdated | cut -d' ' -f 1 | sed '1d' | xargs -I '$' echo '$latest' | xargs echo)'
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
