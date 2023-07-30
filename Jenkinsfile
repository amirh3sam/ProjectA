pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
     // Some build steps here
    //Clears the target directory and builds the project and packages the resulting JAR file into the target directory - without running the unit tests during the build.
               bat  'mvn clean package -Dmaven.test.skip=true'
               
            }
        }

        stage('Test') {
            steps {
                // Some test steps here
                //run only the smoke tags
              bat 'mvn test'
              

            }
        }
        stage('Archive artifact the Jar file') {
            steps {
      //Archive the JAR file as an artifact after build:
      //The artifact can be easily downloaded and shared with others like for testing or analysis.
       archiveArtifacts 'target/*.jar'
            copyArtifacts(projectName: 'ProjectB', target: 'libs\\\\', flatten: true)
            bat "java -jar libs\\ProjectA-1.0-SNAPSHOT.jar"
            }
        }
    }

}

