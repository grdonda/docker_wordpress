# docker wordpress
projeto para rodar wordpress com dominio customizado via https

** importante
habilite o volume para persistir os dados

## dados do projeto
### maria db: banco de dados
```
base de dados: wordpress
username: wpadmin
password: wpadmin
hostname: mariadb #nome do serviço
```

### arquivo hosts
```
# adicionar no arquivo hosts
127.0.0.1 wordpressteste.com.br
```


### certificado autoassinado
comando para executar localmente para gerar o certificado local auto assinado

### arquivo de configuração
acesse ./nginx/certs e visualize o arquivo openssl.cnf e configure como desejar

```
# acesse a pasta
cd ./nginx/certs

# rode o comando
openssl req -x509 -newkey rsa:2048 -nodes -keyout nginx.key -out nginx.crt -days 365 -config openssl.cnf
```

### importe o certificado
clique com o botão direito no certificado e instale em seu sistema operacional

