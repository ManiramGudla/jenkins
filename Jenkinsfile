pipeline{
  agent any
  env{
     
    branch={params.branch}
    host='ubuntu'
    ip={params.hostIp}
    stages{
    
      stage('git clone'){
        step{
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


}
