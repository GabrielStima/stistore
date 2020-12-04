
# STI Store Overview

A STI Store é uma loja de roupas casuais que constitui de um site responsivel e um aplicativo mobile.
Para entender mais a fundo sobre as tecnologias e ideias usadas na construção de cada aplicação irá ter um documento especifico.

## Ideia Inicial

Para a construção desse projeto primeiro busquei por inspiração em grandes nomes do mercado de e-commerce com foco em roupas, os sites que foram utilizados para isso foram:
* [Kanui](https://www.kanui.com.br/);
* [Lacoste](https://www.lacoste.com/br/);
* [Renner](https://www.lojasrenner.com.br/);
* [Netshoes](https://www.netshoes.com.br/);

As inspirações mais fortes foram a **Kanui** e a **Lacoste**, a Kanui é uma loja de roupas voltado para o público mais jovem e com uma moda mais *street* mas mesmo assim tem roupas de todos os estilos, e a Lacoste visa um público um pouco mais velho em relação a Kanui com roupas mais sobrias e apostando na marca como o principal chamariz. 
É por conta dessas pequenas diferenças de público e forma de chamar o mesmo, há grandes diferenças nos sites.

## UI/UX

Antes de iniciar o desenvolvimento utilizei como analise de layout UI/UX sites como [Behance](https://www.behance.net/) e [Dribble](https://dribbble.com/) para buscar inspiração para cor e layout.

Foi desenvolvido 3 UI um para o site, um para o site no mobile e um para o aplicativo.

### Wireframe Low Fidelity Desktop

![UI LF Desktop full flux](https://github.com/GabrielStima/stistore/blob/main/Design/UI/lowFidelity/Site/UI%20Site.png)

### Wireframe Low Fidelity Site mobile

![UI LF Site mobile full flux](https://github.com/GabrielStima/stistore/blob/main/Design/UI/lowFidelity/Mobile/UI%20Site%20Mobile.png)

### Wireframe Low Fidelity App

![UI LF App full flux](https://github.com/GabrielStima/stistore/blob/main/Design/UI/lowFidelity/App/UI%20App.png)

E após ter um conceito de site, fiz a analise da paleta de cores e da fonte que seria usada no layout.

### Guia de cores e fontes

![UI Color and fonts guide](https://github.com/GabrielStima/stistore/blob/main/Design/UI/ColorAndFonts/ColorAndFonts.png)

As cores principais usadas foram o azul(#173957) e o branco(#FFFFFF), escolhidas com o intuito de passar aos cliente confiança e clareza seguindo os conceitos da teoria das cores em relação ao marketing. E com isso decidito consegui dar seguimento aos wireframes de alta fidelidade.

### Wireframe High Fidelity Desktop

![UI HF Desktop Full Flux](https://github.com/GabrielStima/stistore/blob/main/Design/UI/lowFidelity/Site/UI%20Site.png)

### Wireframe High Fidelity Site mobile

![UI HF Site mobile Full Flux](https://github.com/GabrielStima/stistore/blob/main/Design/UI/lowFidelity/Mobile/UI%20Site%20Mobile.png)

### Wireframe High Fidelity App

![UI HF App Full Flux](https://github.com/GabrielStima/stistore/blob/main/Design/UI/highFidelity/App/UX%20App.png)

## INFRASTRUCTURE

Para desenvolver essa aplicação foi escolhido para hospedagem o **Heroku** e por ele ter vários recursos interessantes e integrados como banco de dados foi escolhido o **Postgres**, para armazenar os dados, usando a estrutura SQL e para facilitar o manuseio do **Postgres**, irá ser usado o **Knex** que é um *SQL query builder*.

### Banco de Dados

Conforme falado acima será utilizado o **Postgres**, porem dentro do próprio **Heroku** temos a possibilidade de criar mais de um banco de dados para o mesmo projeto por isso teremos 2 BD, uma para DEV e outro para ambiente de TEST.

### Armazenamento das Imagens

Por conta do tamanho limitado que os bancos de dados podem ter iremos usar um armazenamento externo dedicado as imagens, usaremos o **Cloudinary**.

### Porque um SQL Buider?

A ideia desse projeto é apresentar as pessoas as habilidades do desenvolvedor, entretanto pensando na parte de testes será necessario um ambiente inteiro, para garantir a não interferencia dos dados entre o ambiente de DEV e o de TEST. E pensando nisso e na facilidade de criar um ambiente novo caso preciso, iremos utilizar *Migrations*, para termos o versionamento do schema.
