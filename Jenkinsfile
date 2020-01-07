node('master')
{
    stage('ContinuousDownload') 
    {
        git 'https://github.com/arunreddy00/multiranch.git'
    }
    stage('ContinuousBuild')
    {
        sh label: '', script: 'mvn package'
    }
    stage('ContinuousDeployment')
    {
        sh label: '', script: '''scp /home/ubuntu/.jenkins/workspace/naga_loans/webapp/target/webapp.war  ubuntu@13.229.249.25:/var/lib/tomcat8/webapps/nagatest.war
'''
    }
    
    
    
    
    
    
    
    
    
    
}
