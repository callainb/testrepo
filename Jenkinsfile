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
          docker.image('hello-world').inside {
            sh 'ls -la'
            sh 'hostname'
          }
        }
      }
    }
  }
}
