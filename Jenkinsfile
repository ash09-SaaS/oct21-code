node() {
   stage('Download code from git') 
       {
    git branch: 'dev', url: 'https://github.com/ash09-SaaS/oct21-code.git'
       }

stage('convert into artifacts') 
      {
   sh 'mvn package '
      }

stage('Deploy into container ') 
      {
   deploy adapters: [tomcat9(credentialsId: 'd27a8e66-d53f-4e40-a656-1bdc462cabb6', path: '', url: 'http://3.111.29.38:8080/')], contextPath: '/jenkinsdevapp', war: '**/*.war'
      }

}
