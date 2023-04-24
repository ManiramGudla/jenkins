pipeline{
  agent any
  env{
     
    commit_id={params.commit_id}
    branch={params.branch}
    host='ubuntu'
    ip={params._hostIp}
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
