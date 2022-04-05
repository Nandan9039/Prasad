def version = "1.0.0-release"
def artifactId ="demo-app"
def groupId = "com.siemens.devops"
def appName = "demo-app"
def JfrogUrl ="http://localhost:8082/artifactory/logic-ops-lab-libs-release/"



pipeline {
     agent any
  stages {

   stage('checkout'){
   steps{
        script{
          checkout scm
        }
    }
           }
        
   stage('mvnBuild'){
      steps{
      script{
      sh script: "mvn clean install"
      sh "ls -ltrs ./target"
      echo "${version}"
            }
      }
  }
  
  }
  
}
