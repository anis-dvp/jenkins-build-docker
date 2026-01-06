node {
    stage('Clone') {
        git branch: 'main', url: 'https://github.com/anis-dvp/mvn-helloword.git'
    }
    stage('Build') {
        sh '''
            mvn clean package
        '''
    }
    stage('Run') {
        sh '''
            java -jar target/demo-maven-1.0-SNAPSHOT.jar
        '''
    }
}
