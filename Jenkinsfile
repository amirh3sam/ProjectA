
pipeline {
    agent any
    
    stages {
        stage('Trigger ParameterizedChrome') {
            steps {
                script {
                    def browserValue = 'chrome'
                    def environmentValue = '@smoke'
                    
                    // Trigger the ParameterizedJob with specified parameters
                    build job: 'mySmokePipeLine', parameters: [
                        string(name: 'browser', value: browserValue),
                        string(name: '@testType', value: environmentValue)
                    ]
                }
            }   
        }
                stage('Trigger ParameterizedFirefox') {
            steps {
                script {
                    def browserValue2 = 'firefox'
                    def environmentValue = '@smoke'
                    
                    // Trigger the ParameterizedJob with specified parameters
                    build job: 'mySmokePipeLine', parameters: [
                        string(name: 'browser', value: browserValue2),
                      string(name: '@testType', value: environmentValue)
                    ]
                }
            }   
        }
    }
}


