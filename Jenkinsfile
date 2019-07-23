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
                          expresssion { params.REQUESTED_ACTION == 'dev'}  
                       // {
                        //  branch "master"
                      //}
                         
                 }
                 steps {
                       echo "Hello"
                 }
                 }
          }
}
