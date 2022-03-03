# APIsicred

Projeto baseado em Maven na IDE Eclipse com linguagem Java, Selenium Web Driver e RestAssured.

## Configurações

- openjdk version "11.0.13"
- junit "4.12"
- selenium-java "3.141.59"
- rest-assured "4.0.0"
- Eclipse IDE "Versão - 2021-06"

## Add your files

- [ ] [Create](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#create-a-file) or [upload](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#upload-a-file) files
- [ ] [Add files using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html#add-a-file-using-the-command-line) or push an existing Git repository with the following command:

```
cd existing_repo
git remote add origin https://gitlab.com/VitorRobertoOliveira/apisicred.git
git branch -M main
git push -uf origin main
```

## Instalação

- Realizar o clone do projeto através do link: https://gitlab.com/VitorRobertoOliveira/apisicred.git
- Rodar o projeto através da classe: class RunTest.java, que está contida no package "runner"

## Observações

### As anotações abaixo diferem da documentação com as regras da API;
- Aceita campo CPF diferente da regra ("999.999.999-99"), aceita caracteres especiais e aceita letras assim como aceita o campo vazio;
- Aceita campo "parcelas" com valores maiores que 48;
- Aceita campo "valor" com valores menores que R$ 1000,00;
- Aceita campo "seguro" com valores diferentes de "true" ou "false";
- Uma simulação para um mesmo CPF retorna um HTTP Status 400 e não 409 como está descrito na regra, e a mensagem na response body também é diferente;
- O Delete com sucesso retorna o HTTP Status 200 e não 204 como está descrito na documentação;
- Não consegui reproduzir o cenário onde o Delete retorna o HTTP Status 404 com a mensagem "Simulação não encontrada", pois mesmo não existindo a simulação pelo ID informado a response body é "OK";
