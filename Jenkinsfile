pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                bat "mvn clean package"
            }
        }
         stage("Deploye"){
            steps{
                deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'be387ed4-1fde-4be6-b24e-1261dc000255', path: '', url: 'http://localhost:8081')], contextPath: 'myfirstpipelinejob', war: '**/jenkin-0.0.1-SNAPSHOT.war'
            }
        }
    }
}
