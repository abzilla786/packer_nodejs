# Packer for nodejs

This packer creates an AMI that is provisioned using the nodejs cookbook. This creates a perfect testing environment for nodejs and can be used to spin up many machines with the same environment.

## pre-requisites
- Packer
- aws credetials
- pem key
- atom

## how to install

to start the installation process, download or clone the git repo and go to the folder location on your terminal.

run the command:
```
berks vendor
```
this will download the relevant cookbook files for the packer to use later on in the build stage.

now you must validate the packer file using the command:
```
packer validate packer_nodejs.json
```
your should expect to see a validate successful message in terminal.

now to build the AMI you run the command:
```
packer build packer_nodejs.json
```
this should run correctly without any problems, once completed you can check your AMI on AWS in the AMI section.
