pipeline{
    agent any
     tools {
        git 'Git_Default'  // The name you gave your Git tool configuration
    }
    stages{
        stage("Build"){
            steps{
                sh "mvn -DskipTests clean package"
            }
        }
         stage("Test"){
            steps{
                sh "mvn test"
            }
        }
    }
}
