
## Entrega do projeto 2 BIM

# Projeto de Envio de Email


 Este é um projeto criado com Java e Spring Boot para enviar email utilizando o Gmail.
 

## 1 Criar aqruivo jar

    mvn clean package

## 2 Executando o projeto

- Utilizando o arquivo jar

```
    export SPRING_EMAIL_USERNAME=usuario1.feltex@gmail.com
    export SPRING_EMAIL_PASSWORD=********************

    java -jar target/ServicoEmail.jar 
```

- Utilizando o maven

```
    export SPRING_EMAIL_USERNAME=usuario1.feltex@gmail.com
    export SPRING_EMAIL_PASSWORD=********************
    
    mvn spring-boot:run
```


## Deu erro? Tente:

1. Erro de acesso `535-5.7.8 Username and Password not accepted.`  

```
 # Caused by: org.springframework.mail.MailAuthenticationException: Authentication failed; nested exception is javax.mail.AuthenticationFailedException: 535-5.7.8 Username and Password not accepted. Learn more at
 # 535 5.7.8  https://support.google.com/mail/?p=BadCredentials m35sm5842510wms.1 - gsmtp
```

1. Confirme se usuário e senha estão corretos.
2. Desabilite a verificação em 2 [etapas](https://support.google.com/accounts/answer/1064203?hl=pt-BR&co=GENIE.Platform%3DDesktop)
3. Para enviar email em sua aplicação você precisa habilitar uma configuração de segurança no Gmail
   1. Habilitando aplicações menos Seguras no GMail[detalhes](https://support.google.com/accounts/answer/6010255?hl=pt).
