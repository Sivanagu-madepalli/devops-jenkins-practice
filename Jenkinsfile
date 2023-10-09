node {
    try {
        agent {
            docker {
                image 'maven:3.6.3'
            }
        }
        
        stages {
            stage('Build') {
                steps {
                    sh 'mvn clean install'  // Assuming you want to build with Maven
                    echo "Build"
                }
            }
            stage('Test') {
                steps {
                    echo "Test"
                }
            }
            stage('Integration Test') {
                steps {
                    echo "Integration Test"
                }
            }
        }

        post {
            always {
                echo "Running always"
            }
            success {
                echo "Running when successful"
            }
            failure {
                echo "Running when fail"
            }
        }
    } catch (Exception e) {
        currentBuild.result = 'FAILURE'
        throw e
    }
}
