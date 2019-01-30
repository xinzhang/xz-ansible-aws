### dependencies
sudo su
python2.7 get-pip.py
python2.7 -m pip install boto3
pip install boto3

sudo easy_install nose
sudo easy_install tornado
sudo python2.7 -m pip install nose tornado

## execute
ansible-playbook -i hosts demo-ec2-key.yaml
ansible-playbook -i hosts demo.yaml

## connect
ssh -i "demo-ec2-key.pem" ec2-user@ec2-13-239-111-209.ap-southeast-2.compute.amazonaws.com
