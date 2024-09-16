pipeline {
	agent any
	stages {
	  stage('scan') {
	    Step {
	      sh "docker run -v ${WORKSPACE}:/src --workdir /src returntocorp/semgrep-agent:v1 semgrep-agent --config p/ci"
	     }
	   }
	}
   }
