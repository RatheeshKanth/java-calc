node
{
    stage('clonning from GIT'){
	git 'https://github.com/RatheeshKanth/my-simple-java.git'
     }

stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarServer' ;
      withSonarQubeEnv('SonarServer') {
      sh "${scannerHome}/bin/sonar-scanner \
        -D sonar.login=admin \
        -D sonar.password=admin123 \
        -D sonar.projectKey=my-app1 \
        -D sonar.sources=.\
        -D sonar.test=src/test/ \
        -D sonar.exclusions=vendor/**,resources/**,**/*.java \
        -D sonar.host.url=http://3.91.72.68:9000/"
        }
}
}