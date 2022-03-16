# Introdução

## O que é Docker?

- O **Docker** é um software que **reduz a complexidade de setup** e aplicações;
- Onde **configuramos containers**, que são como servidores para rodar nossas aplicações;
- Com facilidade, podemos criar **ambientes independentes** e que funcionam em diversos SO’s;
- E ainda deixa os projetos **performáticos**;

---

## Por que Docker?

- O **Docker** proporciona mais velocidade na configuração do ambiente de um dev;
- **Pouco tempo gasto em manutenção**, containers são executados como configurados;
- **Performance** para executar aplicação, mais performático que uma VM;
- Nos livra da **Matrix from Hell**;

---

## Conhecendo a Matrix from Hell

Simplificando, é o desafio de empacotar qualquer aplicativo, independentemente do idioma/frameworks/dependências, para que ele possa ser executado em qualquer nuvem, independentemente dos sistemas operacionais/hardware/infraestrutura.

---

## Qual versão utilizar?

- O **Docker** é dividido em duas versões: **CE x EE**;
- CE é a **Community Edition**, edição gratuita, que nos possibilita utilizar o Docker normalmente, é a que vamos optar;
- EE é a **Enterprise Edition**, edição paga, há uma garantia maior das versões que são disponibilizadas e você tem suporte do time do Docker.

---

## Testando o Docker

```docker
docker run docker/whalesay cowsay Hello_world
```

docker run - incia uma imagem

docker/whalesay - busca o autor (autor) e a imagem (whalesay)