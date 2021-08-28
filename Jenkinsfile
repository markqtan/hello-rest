println "this: ${this}, params: ${params.version}"

def newParams = [];
newParams.add(new StringParameterValue("EPL_RELEASE_NUMBER", "init"))
try {
    $build().addOrReplaceAction($build().getAction(ParametersAction.class).createUpdated(newParams))
} catch (err) {
    $build().addOrReplaceAction(new ParametersAction(newParams))
}


final VERSION = params.version;

//@Library("jenkinslib@${VERSION}")_
//import hello.HelloGroovy;

final lib = library("jenkinslib@${params.version}").hello;
println lib.HelloGroovy.test(this, "Mark");

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
          //println new lib.hello.HelloGroovy().hi("Mark");
        }
      }
    }

  }
}
