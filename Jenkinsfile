pipeline {
    agent any
    environment {
		myrepo='spring-boot-mongodb-react-crud/web/'
    }

    stages {
        stage ('build') {
			steps {
                sh "mvn clean package -f $myrepo/pom.xml"
			}
            
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