pipeline {
    agent wind-node

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven3.3.3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven3.3.3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('install Stage') {
            steps {
                withMaven(maven : 'maven3.3.3') {
                    sh 'mvn install'
                }
            }
        }
    }
}
