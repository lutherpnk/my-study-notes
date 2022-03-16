# Trabalhando com Containers

<aside>
✏️ Sumário:

- [x] *O que são containers?*
- [x] *Container x Imagem*
- [x] *Onde encontrar imagens*
- [x] *Verificar containers executados*
- [x] *Executar container com interação*
- [x] *Container x VM*
- [x] *Executar container em background*
- [x] *Expor portas*
- [x] *Parando container*
- [x] *Iniciando/reiniciando container*
- [x] *Definindo nome do container*
- [x] *Acessando os logs de um container*
- [x] *Removendo container*
</aside>

---

## O que são containers?

- Um pacote de código que pode executar uma ação, por exemplo: rodar uma aplicação de Node.js, PHP, Python e etc;
- Ou seja, os nossos projetos serão executadas dentro dos containers que criarmos/utilizarmos;
- Containers utilizam imagens para poderem ser executadas;
- Múltiplos containers podem rodar juntos, exemplo: um para PHP e outro para MySQL.

---

## Container x Imagem

- Imagem e Container são recursos fundamentais do Docker;
- Imagem é o “projeto” que será executado pelo container, todas as intruções estarão declaradas nela;
- Container é o Docker rodando alguma imagem, consequentemente executado algum código proposto por ela;
- O fluxo é: programamos uma imagem e a executamos por meio de um container;

---

## Onde encontrar imagens

- Vamos encontrar imagens no repositório do Docker: [**Docker Hub**](https://hub.docker.com/);
- Neste site podemos verificar quais as imagens existem da tecnologia que estamos procurando, por exemplo: Node.js;
- Vamos executar uma imagem em um container com o comando:

```docker
docker run <imagem>
```

---

## Verificar containers executados

- O comando “docker ps” ou “docker container ls” exibe quais containers estão sendo executados no momento;
- Utilizando a flag “-a”, temos também todos os containers já executados na máquina;
- Este comando é util para entender o que está sendo executado e acontece no nosso ambiente;

---

## Executar container com interação

- Podemos rodar um container e deixá-lo executando no terminal;
- Vamos utilizar a flag “-it”;
- Desta maneira podemos executar comandos disponíveis no container que estamos utilizando o comando run;

---

## Container x VM (Virtual Machine)

- Container é uma aplicação que serve para um determinado fim, não possui sistema operacional, seu tamanho é de alguns mbs;
- VM possui sistema operacional próprio, tamanho de GBs, pode executar diversas funções ao mesmo tempo;
- Containers acabam gastando menos recursos para serem executados, por causa do seu uso específico;
- VMs gastam mais recursos, porém podem exercer mais funções.

---

## Executar container em background

- Quando iniciamos um container que persiste, ele fica ocupando o terminal;
- Podemos executar um container em background, para não precisar ficar com diversas abas de terminal aberto, utilizamos a flag “-d” (detached);
- Verificamos containers em background com docker ps também.

```docker
docker run nginx
# Dessa forma o container será executado, porém o terminal ficará ocupado.
# Para evitar esse caso, é necessário usar a flag "-d"
docker run -d nginx
```

---

## Expor portas

- Os containers de docker não tem conexão com nada de fora deles;
- Por isso precisamos expor portas, a flagé a “-p” e podemos fazer assim:

```docker
docker run -d -p 80:80 <imagem>
```

- Desta maneira o container estará acessível na porta 80;

---

## Parando containers

- Podemos parar um container com o comando:

```docker
# Para parar um container:
docker stop <id ou nome>
```

- Desta maneira esateremos liberando recursos que estão sendo gastos pelo mesmo;
- Podemos verificar os containers rodando com o comando docker ps;

---

## Iniciando/reinciando container

```docker
docker start <id>
```

---

## Definindo nome do container

- Podemos definir um nome do container com a flag “--name”;
- Se não colocamos, recebemos um nome aleatório, o que pode ser um problema para uma aplicação profissional;
- A flag “run” é inserida junto do comando run.

---

## Acessando os logs de um container

- Podemos verificar o que aconteceu em um container com o comando logs;
- Utilizamos da seguinte maneira:

```docker
docker logs <id>
```

- As últimas ações realizadas no container, serão exibidas no terminal.

---

## Removendo container

- Podemos remover um container da máquina que estamos executando o Docker;

```docker
# O comando é:
docker -rm <id>
```

- Se o container estiver rodando ainda, podemos utilizar a flag “-f” (force);
- O container removido não é mais listado em “docker ps -a”