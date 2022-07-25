pipeline {
    agent any
    stages {
        	stage ("Python Bandit Security Scan"){
			    steps{
				sh "docker run --rm --volume \$(pwd) secfigo/bandit:latest"
			    }
		    }
		    stage ("Dependency Check with Python Safety"){
			    steps{
				sh "docker run --rm --volume \$(pwd) pyupio/safety:latest safety check"
				sh "docker run --rm --volume \$(pwd) pyupio/safety:latest safety check --json > report.json"
			    }
		    }
		    stage ("Static Analysis with python-taint"){
			    steps{
				sh "docker run --rm --volume \$(pwd) vickyrajagopal/python-taint-docker pyt ."
			    }
		    }
    }
}
