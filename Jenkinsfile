pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS445 PES1UG20CS445-1.cpp'
                echo 'Successfully Compiled .cpp file'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS445'
                echo 'Successfully Printed Output of .cpp file'
                //Below Code used for creating intentional error
//                 post {
//                     failure {
//                         echo "Unable to Execute .cpp file"
//                     }
//             }
        }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            
        }
    }
    }
    post {
        failure {
            //echo "pipeline failed"
            error "Pipeline Failed"
            }
        }
    }
