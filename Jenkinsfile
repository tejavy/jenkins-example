pipeline {
    agent any
    tools {
        maven
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven {
                    sh 'mvn deploy'
                }
            }
        }
    }
} 
