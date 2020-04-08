node{
stage('SCM Check out'){
git 'https://github.com/naveen-hs/SimpleMavenWebApp'
}
stage('Compile and package'){
  def mvnHome=tool name: 'Maven', type: 'maven'
sh "${mvnHome}/bin/mvn package"
} 
  stage('Deploy on tomcat'){
 sh "cp /var/lib/jenkins/workspace/GitWithMaven/target/*.war /var/lib/tomcat8/webapps/"
  }
}

