pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "oraclejdk8"
    }

    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin123'
        RELESE_REPO = 'vprofile-relese'
        CENTRAL_REPO = 'vpro-maven-central1'
        NEXUSIP = '172.31.28.104'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('BUILD'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}