pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                echo 'make' 
            }
        }
        stage('Test'){
            steps {
                echo 'make check'
                junit 'reports/testReport.xml' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'make publish'
            }
        }
    }
}
