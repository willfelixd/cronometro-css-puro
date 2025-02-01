# cronometro-css-puro

## Criacao do Projeto

Criar uma pasta para o projeto:

```sh
mkdir cronometro-css-puro && cd cronometro-css-puro
```

Criar os arquivos `index.html` e `main.css` dentro da pasta `cronometro-css-puro`.

Criar um `Dockerfile` para definir a imagem Docker.

## Criacao do Dockerfile

Criar um arquivo `Dockerfile` na raiz do projeto com o seguinte conteúdo:

```Dockerfile
# Usa uma imagem base do Nginx
FROM nginx:latest

# Copia os arquivos para a pasta padrão do Nginx
COPY . /usr/share/nginx/html

# Expõe a porta 80 para acesso
EXPOSE 80
```

## Construindo a Imagem Docker

Executar o seguinte comando para construir a imagem Docker:

```sh
docker build -t willfelixd/cronometro-css-puro:1.0 .
```

Substituir `usuario` pelo seu nome de usuário no Docker Hub.

## Testando a Imagem Localmente

Rodar um container localmente para testar a aplicação:

```sh
docker run -d -p 8080:80 usuario/projeto:1.0
```

A aplicação estará disponível em: [http://localhost:8080/](http://localhost:8080/).

## Criacao de um Repositorio no GitHub

Criar um repositório no GitHub.

Inicializar o Git no projeto:

```sh
git init
```

Adicionar os arquivos e commitar:

```sh
git add .
git commit -m "Versão inicial"
```

Adicionar o repositório remoto e fazer push:

```sh
git remote add origin https://github.com/willfelixd/cronometro-css-puro.git
git branch -M main
git push -u origin main
```

## Publicando a Imagem no Docker Hub

Logar no Docker Hub:

```sh
docker login
```

Enviar a imagem para o Docker Hub:

```sh
docker push usuario/projeto:1.0
```

## Executando a Imagem a Partir do Docker Hub

Em qualquer máquina com Docker instalado, executar:

```sh
docker run -d -p 8080:80 willfelixd/cronometro-css-puro:1.0
```

Agora a aplicação está acessível via [http://localhost:8080/](http://localhost:8080/).

## Conclusao

Este README documenta os passos para criar, versionar e publicar uma aplicação web simples com Docker e Docker Hub.

