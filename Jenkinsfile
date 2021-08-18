@Library('jenkinslib@2.0')_
import hello.HelloGroovy;

pipeline {
  agent any
  stages {
    stage('') {
      steps {
        echo 'hello world'
        script {
          println new HelloGroovy().hi("Mark");
        }
      }
    }

  }
}
