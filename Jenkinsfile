pipeline {
  agent any
  tools{
  maven "Maven 3.6.3"  
  }
  stages{
      stage("build"){
          steps{
              echo 'compiling'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'testing'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'packaging'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
