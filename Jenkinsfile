pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven3.9.4') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Maven3.9.4') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Installation Stage') {
            steps {
                withMaven(maven : 'Maven3.9.4') {
                    sh 'mvn install'
                }
            }
        }
    }
}
