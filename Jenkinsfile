pipeline{
  agent {dockerfile true}
  stages {
    stage("build"){
      steps{
        echo 'biuilding the application'
	sh 'docker build -t test-jenkins:latest .'
        echo 'there was some modification'
      }
    }
    stage("test"){
      steps{
        echo 'testing the application'
      }
    }
    stage("deploy"){
      steps{
        echo 'deploying the application'
	sh 'docker run test-jenkins'
      }
    }
  }
}
