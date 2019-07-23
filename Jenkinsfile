pipeline {
         agent any
         parameters {
                  choice (
                           choices: ['dev','stage'],
                           description: '',
                           name: 'REQUESTED_ACTION')
         }                   
                           
                  
         
         stages {
                 stage('One') {
                 steps {
                     echo 'Hi, this is Ramesh from Academy'
                 }
                 }
                 stage('Two') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Three') {
                 when {
                          expression { params.REQUESTED_ACTION == 'dev'}  
                                              
                 }
                 steps {
                       echo "Moved to Development"
                 }
                 }
                stage('Four') {
                 parallel { 
                           stage('Unit Test') {
                           steps {
                                echo "Running the unit test..."
                           }
                            }
                          stage('Integration test') {
                               steps {
                                echo "Running the integration test..."
                              }
                          }
                          }
          }
}
