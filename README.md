# pulp-research

$> sudo yum install http://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm   

### MongoDB
$> sudo yum install mongodb-server  
$> sudo service mongod start  

### Message Broker
$> sudo yum install qpid-cpp-server qpid-cpp-server-linearstore  
$> yum install cyrus-sasl-plain  
$> sudo service qpidd start  

### Pulp
$> sudo yum install pulp-server python-gofer-qpid python-qpid qpid-tools  
$> sudo vim /etc/yum.repos.d/rhel-pulp.repo  
$> sudo yum install pulp-server python-gofer-qpid python-qpid qpid-tools  
  
$>  sudo vim /etc/pulp/server.conf      
$>  sudo -u apache pulp-manage-db      
$>  sudo service httpd start  
$>  sudo service pulp_workers start     
$>  sudo service pulp_celerybeat start   
$>  sudo service pulp_resource_manager start   

### admin-client [Open Url](http://docs.pulpproject.org/user-guide/admin-client/index.html)
$>  sudo yum install pulp-admin-client pulp-rpm-admin-extensions pulp-puppet-admin-extensions pulp-docker-admin-extensions   
$>  sudo vim /etc/pulp/admin/admin.conf    
$>  pulp-admin list   
    
$>  sudo yum install pulp-consumer-client pulp-rpm-consumer-extensions pulp-puppet-consumer-extensions pulp-agent pulp-rpm-handlers pulp-rpm-yumplugins pulp-puppet-handlers python-gofer-qpid   
$>  sudo vim /etc/pulp/consumer/consumer.conf     
$>  sudo service goferd start    
$>  pulp-admin repo --help    
     
$>  pulp-admin login -u admin    
$>  sudo yum install pulp-rpm-plugins.noarch    
$>  pulp-admin rpm repo create --repo-id=foo    
$>  pulp-admin repo list    
    
$>  sudo yum install pulp-rpm-plugins    
    
$>  sudo vim /etc/pulp/server/plugins.conf.d/    
$>  vim /etc/pulp/server/plugins.conf.d/    
    
$>  sudo apachectl stop    
$>  sudo yum install pulp-rpm-plugins     
     
$>  sudo yum install pulp-rpm-admin-extensions    
