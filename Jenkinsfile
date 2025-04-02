pipeline {
    agent any
    tools {
        jdk "JDK21"
        maven "MAVEN3.9"
    }
    
    environment {
        SNAP_REPO = 'vprofile-snapshot'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'Bakumba2@'
		RELEASE_REPO = 'vprofile-release'
		CENTRAL_REPO = 'vpro-maven-central'
		NEXUSIP = '172.31.84.102'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'

    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}