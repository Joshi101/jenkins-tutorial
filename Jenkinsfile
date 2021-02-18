pipeline{
  agent any
  environment{
	IMAGE_NAME = 'flask-demo'
}
  stage("Clean"){
      steps{
        sh "docker rm -f \$(docker ps -a -q  --filter ancestor=${IMAGE_NAME}) &>/dev/null && echo 'removed container' || echo 'nothing to remove'"
      }
    }
  stages {
    stage("build"){
      steps{
        echo 'biuilding the application'
        sh 'docker build -t ${IMAGE_NAME} .'
      }
    }
    stage("test"){
      steps{
        echo 'testing the application'
      }
    }
    stage("deploy"){
      steps{
        sh 'docker run -p 5001:5000 -d ${IMAGE_NAME}'
      }
    }
  }
}
