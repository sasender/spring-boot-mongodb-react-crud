pipeline {
    agent any
    environment {
		myrepo='spring-boot-mongodb-react-crud/web/'
    }
    
    tools  {
		maven 'm3.6'
	}

    stages {
        stage ('build') {
            sh "mvn clean package -f $myrepo/pom.xml"
        }

        stage ('testresults'){
			steps {
				junit "$myrepo/target/surefire-reports/*.xml"
			}
		}
		stage ('archive actifacts'){
			steps {
				archiveArtifacts artifacts:"$myrepo/target/*.?ar/", followSymlinks: false
			}
		}
    }
}