pipeline {
   agent any
   tools{
        maven 'maven'
    }
   stages {
    stage('GIT') {
      steps {
           // The below will clone your repo and will be checked out to master branch by default.
           git credentialsId: 'gitgouuri', url: 'https://github.com/gouuri/hello-world.git'
       }
    }
    stage('mvn Build') {
      steps {
        sh "cd /var/lib/jenkins/workspace/dec1"  
        sh "mvn clean install"
       }
    }
  }
}
