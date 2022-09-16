# Curso Ansible para SysAdmin

Para o curso, foram provisionados containers com imagens Ubuntu via docker compose.

```
docker compose up -d
```

- Criar novo par de chaves para autenticacao via chave ssh
```
ssh-keygen -b 2048 -t rsa -f ansible-key
```

- Copiar chave publica para o host alvo
```
ssh-copy-id -i [nome-da-chave] [user]@[ip-do-host]
```
```
ssh-copy-id -i [nome-da-chave] [user]@[ip-do-host]
```

- Acessar container usando o arquivo da chave ssh
```
ssh -i [nome-da-chave] [user]@[ip-do-host]
```

- Permitir acesso sem passar arquivo publico via linha de comando

```
vi ~/.ssh/config
```
Usar seguintes parâmetros:
```
#ansible
IdentityFile "~/.ssh/[chave-privada]"
```

- Instalacao do ansible via pip
```
sudo yum install python3-pip
pip3 install pip --upgrade
pip3 install ansible
```
Realizar logout para recarregar os binarios

- Ajustar path

```
vi /etc/profiles
```

- Atualizar o ansible via pip
```
pip install ansible --upgrade
```