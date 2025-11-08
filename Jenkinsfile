pipeline {
    // Use a Docker container with Maven as the build environment
    agent {
        docker { image 'maven:3.8-jdk-11' }
    }

    stages {
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Build') {
            steps {
                // Build the .jar or .war file
                sh 'mvn package'
            }
        }
        stage('Test') {
            steps {
                // Run all automated tests
                sh 'mvn test'
            }
        }
    }
}
