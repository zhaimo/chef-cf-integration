# chef-cf-integration
aws cloudformation create-stack --stack-name stackname --template-body file://cf-chef-unattended-bootstraps-need-paramfile.json --parameters ParameterKey=UserData,ParameterValue=$(base64 -w0 userdata.sh) --capabilities CAPABILITY_IAM

aws cloudformation create-stack --stack-name stackname --template-body file://cf-chef-unattended-bootstraps-no-paramfile.json  --capabilities CAPABILITY_IAM
