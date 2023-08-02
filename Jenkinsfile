
pipeline {
    agent any
    
    stages {
        stage('Trigger ParameterizedJob') {
            steps {
                script {
                    def browserValue = 'chrome'
                    def browserValue2 = 'firefox'
                    def environmentValue = '@smoke'
                    
                    // Trigger the ParameterizedJob with specified parameters
                    build job: 'ParameterizedJob', parameters: [
                        string(name: 'browser', value: browserValue),
                             string(name: 'browser', value: browserValue2),
                        string(name: '@testType', value: environmentValue)
                    ]
                }
            }
        }
    }
}


