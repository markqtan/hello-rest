@Library('jenkinslib')_
import hello.HelloGroovy;

pipeline {
  agent any
  environment {
    LIB_VERSION="2.0"
  }
  parameters {
        string(name: 'version', defaultValue: '1.0', description: 'shared lib version')
  }
  stages {
    stage('') {
      steps {
        echo 'hello world'
        script {
          println "DEBUG: parameter version = ${params.version}"
          println new HelloGroovy().hi("Mark");
        }
      }
    }

  }
}
