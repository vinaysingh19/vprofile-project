pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
     environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS-PASS = 'admin123'
        RELEASE-REPO = 'vprofile-release'
        CENTRAL-REPO = 'vpro-maven-central'
        NEXUS-GRP-REPO = 'vpro-maven-group'
        NEXUSIP = '172.31.7.52'
        NEXUSPORT = '8081'
        NEXUS_LOGIN = 'nexuslogin' 
     }

    stages {
        stage('Build'){
          steps {
            sh 'mvn -s setting.xml -DskipTests install'
          }  
        }
    }
}