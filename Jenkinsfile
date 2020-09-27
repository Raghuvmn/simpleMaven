node
{
 stage('SCM Checkout')
{
withCredentials(usernamePassword(credentialsId: GIT_CREDS, passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')
git 'https://github.com/Raghuvmn/simpleMaven'
}
stage('Compile-Package')
{
def mvnHome= tool name: 'Maven', type: 'maven'
sh "${mvnHome}/bin/mvn package"
}

}
