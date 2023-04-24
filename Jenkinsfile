pipeline{
  agent any
  environment{
     
    branch={params.branch}
    host='ubuntu'
    ip={params.hostIp}
  }
    stages{
    
      stage('git clone'){
        steps{
          '''
          ssh -oStrictHostKeyChecking=no {host}@{ip}'
          cd /home/ubuntu
          mkdir test
          
          '
           '''  
            }
      }
    
    }


}
