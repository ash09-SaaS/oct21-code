node('slave18') {
   stage('Download code from git') 
       {
    git branch: 'dev', url: 'https://github.com/ash09-SaaS/oct21-code.git'
       }

stage('convert into artifacts') 
      {
   sh 'mvn package '
      }


}
