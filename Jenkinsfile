pipeline
{
agent any
environment
{
 dockerImage='meghh'
 registry='meghanamurthyy/myapp-repo'
 registryCredential='docker_hub_cred'
}
stages{
 stage('Checkout')
 {
 steps{
 checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 
'https://github.com/Meghanamurthyy/jenkinss.git']])
 }
 }
 stage('Build Docker image')
 {
steps{
 script{
 dockerImage=docker.build registry
 }
 }
 }
 
 }
}
