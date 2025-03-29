pipeline{
  agent any
  stages{
        stage('git scm')
        {
          steps{
            git credentialsId: 'git-cred', url: 'https://github.com/lokiharsha/java-c-p.git'
          }
          
        }
        stage('package'){
      steps{
        sh 'mvn package'
      }
    }
    stage('deploy'){
      steps{
        sh 'java -cp target/java-c-p-1.0-SNAPSHOT.jar com.alto.App'
      }
    
  }
  
  }
}
