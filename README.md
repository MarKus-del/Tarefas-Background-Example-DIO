# Tarefas em background

Este projeto foi feita um simples cadastro fake com nome e email para demonstrar comom funciona tarefas em background utilizando o redis 

# tecnologias

+ nodejs
+ express
+ nodemailer
+ redis
+ bull
+ bull-board
+ password-generator

# O que eu aprendi?

Neste foi demonstrado como criar variaveis de ambientes no codigo e utilizar posteriormente, além de como configurar e montar as queue no banco NoSql Redis para depois serem processados, no qual cada queue apenas estaria enviado um email de para cada user que tenha submetido o cadastro fake

Alem disso tudo foi mostrado como usar o nodemailer um modulo para node enviar email, a como usar o bull-board para ter uma noção das entradas no banco
de dados e a demonstrou uma plataforma para testa envio de email's chamada [mailtrap.io](https://mailtrap.io/.io)

# como rodar

executar comando docker para rodar o redis

~~~bash
    docker run --name redis -p 6379:6379 -d -t redis:alpine
~~~

rodar o projeto

~~~bash
    yarn queue or npm queue

    depois

    yarn start or npm start
~~~

# problemas

O unico problemas que tive foi a questão da dependencia bull-board estava numa versão mais nova, porém ao mudar o package.json para a versão 0.5.0 conseguir rodar o bull-board como o esperava, mas fica a lição para eu estudar a biblioteca para atualizar o projeto ou para criar novos projetos em redis

    
