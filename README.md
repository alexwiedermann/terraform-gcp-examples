### Crie uma chave ssh

ssh-keygen

### Crie um tfvars com suas variaveis

```
echo "gce_ssh_pub_key_file=""\"~/.ssh/id_rsa.pub\"" > default.tfvars
echo "gce_ssh_user=\"centos\"" >> default.tfvars
echo "ip=""\"`curl ident.me`/32\"" >> default.tfvars
```

### Baixe o provider

```
terraform init
```

### Analise o que vai ser criado e aplique

```
terraform plan -var-file=default.tfvars
terraform apply -var-file=default.tfvars
```
