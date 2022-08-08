pipeline {
    agent any

parameters {

           
        choice choices: ['Component','App'], name: 'Type',  description: 'Select the type'
        extendedChoice defaultValue: 'Vtune,Inspector,Advisor', multiSelectDelimiter: ',', name: 'Test', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', value: 'Vtune,Inspector,Advisor', visibleItemCount: 4
           
        choice choices: ['Build & Test', 'Test','Publish'], name: 'BUILDTYPE',  description: 'Type of the build'
        extendedChoice defaultValue: 'Unit Test,Functional Test', multiSelectDelimiter: ',', name: 'Test', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', value: 'Unit Test,Functional Test', visibleItemCount: 3
}
stages {
           stage("Build & Test") {
             steps {
              sh 'echo "Building the app"'
             }
           }
           stage("Test") {
            steps {
             sh 'echo "Testing the app"'
            }
           }
        }  
}  