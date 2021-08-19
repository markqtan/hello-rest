println "this: ${this}, params: ${params.version}"

final VERSION = params.version;

//@Library("jenkinslib@${VERSION}")_
//import hello.HelloGroovy;

final lib = library('jenkinslib@${VERSION}');

pipeline {
  agent any
  parameters {
        string(name: 'version', defaultValue: '1.0', description: 'shared lib version')
  }
  stages {
    stage('') {
      steps {
        echo 'hello world'
        script {
          println "DEBUG: parameter version = ${params.version}"
          println new lib.hello.HelloGroovy().hi("Mark");
        }
      }
    }

  }
}
