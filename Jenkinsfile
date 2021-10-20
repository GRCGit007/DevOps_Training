pipeline {
    agent any
    tools {
    maven '3.8.3'
        }
stages {
	stage('Build') {
	steps {
	sh 'mvn -B -DskipTests clean package'
	sh 'mvn deploy -s settings.xml'
	}
}// End of Build
stage('Test') {
	steps {
		sh 'mvn test'
		junit 'target/surefire-reports/*.xml'
	}
}//end of test

}//End of Stages
}//end pipeline
