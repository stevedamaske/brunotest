# brunotest
Test Project for Bruno Bronosky

To run these packages, you will need to verifiy your AWS default locations and secrets are set for Packer. Further, you will need to remove the "key_name" field in the Terraform config as this is set currently for my AWS space. 

1. Packer files: 
 centos77.json - Centos 7.7 image which is also adding the most recent EPEL release and main packages on build.
 centos74.json - Centos 7.4 image that is NOT updating anything on build. 
 
2. Terraform config file: 
 terraform.tf - Configuration for a "fixed" and "broken" instance, which also will upload the shell script for testing/proving the 25 sec sudo lag. You may adjust the paths as needed for your instance.
 
3. Timing.sh script
 A simpl ebash shell script which runs sudo commands as user "centos" and then outputs a timing of the processes out to a plain text file "timing.txt" 
