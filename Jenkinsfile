pipeline  {
  agent any
  stages {
    stage("Stage1") {
      steps {
        echo "Hello World!"
      }
    }
    stage("Stage2") {
      steps {
        script {
          docker.image('ubuntu:20.04').inside { c ->
            echo "${docker}"
            echo "${env}"
            sh 'ls -la'
            sh 'hostname'
          }
        }
      }
    }
  }
}
