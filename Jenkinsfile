pipeline {
    agent any
    environment{
        PATH = "/opt/maven/bin:$PATH"
    }
    stages{
      stage('build') {
            steps {
               sh 'mvn clean package'
            }
        }
      stage ('SonarQube analysis') {
            environment {
               scannerHome = tool 'Sai-SonarQube-scanner'

            }
            steps {
                 withSonarQubeEnv('Sai-SonarQube-server'){
                     
                      sh "${scannerHome}/bin/sonar-scanner"
              }
        }

     }
  }
}
