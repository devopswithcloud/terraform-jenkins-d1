# Practise 
* VPC<
* Create a terraform script/module to crete 3 vm's (Jenkins, jenkins-slave, sonar, nexus)
* Vm names should be defined by the user. 
* vm argument , like machine type, zone and all should also be mentioned by the user. 
* Once the 3 vms are created, now the below should happen
    * If jenkins vm then nothing should happen
    * if jenkins-slave vn nothing should happen
    * if sonar vm, sonarqube installaiton shoukld be done 
* we should be implemnting using version, resource.tf, variables.tf , terraform.tfvars and if possible try to create multiple environemnts using env.tfvars file 
* multiple env should be having different values based on the env, and those values should be passd dynamincally by the user. 

* once done, create a module for the same 
* integrrate with terraform but, 
    * it should have different env deployment based on the apply command
