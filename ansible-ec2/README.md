# techguru.cloud

Ansible playbook to create EC2 instance.
Note : Security group "AllowSSH" and keypair "newkeys" should be created before you run this playbook

ansible-playbook -i env/hosts aws_ec2.yml

ssh -i ansible-keys.pem ec2-user@13.211.130.156

ansible-playbook -i inventory --private-key=ansible-keys.pem play.yml

ansible-playbook -i inventory play.yml


### ssh add

ssh-agent bash
ssh-add ~/.ssh/keypair.pem

### use open ssl 

openssl genpkey -algorith RSA -aes-256-cbc -outform PEM -out newkeys.pem -pkey_opt rsa_keygen_bits:4096

chmod 0400 yourname.pem
$ ssh-keygen -y -f yourname.pem > yourname.pub
$ chmod 0444 yourname.pub

openssl genrsa -des3 -out newkeys.pem 4096

