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
             when { expression { params.BUILDTYPE == 'Build & Test' }  }
             steps {
              println "\033[34m............Build and Test..............\033[0m"
              echo "Building the app"
             }
           }
           stage("Test") {
            when { expression { params.BUILDTYPE == 'Test' }  }
            steps {
                println "\033[34m............Testing the code..............\033[0m"
                echo "Testing the app"
            }
           }
           stage("Publish") {
            when { expression { params.BUILDTYPE == 'Publish' }  }
            steps {
                println "\033[34m............Dropping the artifacts..............\033[0m"
                echo "Publishing the app"
            }
           }    

        }  
} 
