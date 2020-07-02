pipeline {
    agent any
    environment{
   PATH="/opt/maven/apache-maven-3.6.3/bin:$PATH"
    }
    stages {
        stage("welcome") {
            steps {
                echo "welcome to jenkinsfile"

}
}
        stage("MAVEN-BUILD") {
        steps {
            sh "mvn clean package"
        }
    }
        stage("deploy-to-tomcat"){
            steps {
                echo "welcome to deployment"
                sh """
                deploy adapters: [tomcat8(credentialsId: 'tomcatadmin'
                
                path: ''
                url: 'http://35.223.144.233:8080')] 
                contextPath: null
                war: '**/*.war' 
                """
            }
        }
       
}
}
