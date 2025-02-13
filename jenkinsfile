pipeline {
    agent any
    environment{
        PATH = "/opt/maven/bin:$PATH"
    }

    stages {
        stage('git cloning') {
            steps {
                git url:'https://github.com/Saisrika/sparkjava-war-example.git', branch: 'master'
            }
        }
        stage('build') {
            steps {
               sh 'mvn clean install'
            }
        }
        
    }
}
