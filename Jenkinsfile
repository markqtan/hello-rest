@Library('jenkinslib')_
import hello.HelloGroovy;

pipeline {
  agent any
  parameters {
        string(name: 'foo', defaultValue: 'foo-default', description: 'foo param')
  }
  stages {
    stage('') {
      steps {
        echo 'hello world'
        script {
          println "DEBUG: parameter foo = ${foo}"
          println new HelloGroovy().hi("Mark");
        }
      }
    }

  }
}
