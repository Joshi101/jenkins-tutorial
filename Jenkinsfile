pipeline{
  agent none
  stages {
    stage("build"){
      steps{
        echo 'biuilding the application'
        sh 'docker build -t flask-demo .'
      }
    }
    stage("test"){
      steps{
        echo 'testing the application'
      }
    }
    stage("deploy"){
      steps{
        sh 'docker run flask-demo'
      }
    }
  }
}
