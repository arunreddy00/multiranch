node('master')
{
    stage('ContinuousDownload') 
    {
        git 'https://github.com/arunreddy00/multiranch.git'
    }
    stage('ContinuousBuild_loans')
    {
        sh label: '', script: 'mvn package'
    }
    stage('ContinuousDeployment_loans')
    {
        sh label: '', script: '''scp /home/ubuntu/.jenkins/workspace/naga_loans/webapp/target/webapp.war  ubuntu@172.31.31.135:/var/lib/tomcat8/webapps/nagatest.war
'''
    }
    
    
    
    
    
    
    
    
    
    
}
