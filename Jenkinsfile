pipeline {
         agent any
         parameters {
                  choice (
                  choices: ['greetings','silence'],
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
                       //not {
                          //  branch "master"
                     //  }
                          expression { params.REQUESTED_ACTION='greetings'}
                 }
                 steps {
                       echo "Hello"
                 }
                 }
          }
}
