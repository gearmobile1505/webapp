pipeline {
    agent any
    stages {
        stage('Initialize') {
            steps {
                script {
                    // Tool configuration for Maven
                    tools {
                        maven 'Maven'
                    }
                    // Additional environment setup
                    sh '''
                        echo "PATH = ${PATH}"
                        echo "M2_HOME = ${M2_HOME}"
                    '''
                }
            }
        }
    
        stage('Build') {
            steps {
                script {
                    // Tool configuration for Maven
                    tools {
                        maven 'Maven'
                    }
                    // Run Maven commands
                    sh 'mvn clean package'
                }
            }
        }
    }
}
