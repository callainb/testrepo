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
            echo "${it}"
            sh 'ls -la'
            //sh 'hostname'
          }
        }
      }
    }
  }
}
