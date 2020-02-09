# Crie uma chave ssh
ssh-keygen

# Crie um tfvars com suas variaveis
```
echo "gce_ssh_pub_key_file=""\"`cat ~/.ssh/id_rsa.pub`\"" > default.tfvars
echo "gce_ssh_user=\"centos\"" >> default.tfvars
```
