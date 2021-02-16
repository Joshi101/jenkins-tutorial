pipeline{
  agent any
  stages {
    stage("build"){
      steps{
        echo 'biuilding the application'
	docker build -t my-flask-image:latest .
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
	docker run
      }
    }
  }
}
