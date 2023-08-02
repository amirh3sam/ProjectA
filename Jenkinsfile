
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
                    build job: 'mySmokePipeLine', parameters: [
                        string(name: 'browser', value: browserValue2),
                             string(name: 'browser', value: browserValue1),
                        string(name: '@testType', value: environmentValue)
                    ]
                }
            }
        }
    }
}


