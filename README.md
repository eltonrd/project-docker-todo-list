# Boas vindas ao repositório do projeto Docker Todo List!

Esse projeto foi desenvolvido durante o módulo de _BackEnd_ na Trybe! #vqv 🚀

Aqui você vai encontrar os detalhes de como foi o desenvolvimento do projeto e quais foram os requisitos obrigatórios e opcionais para o desenvolvimento.

---
# Habilidades desenvolvidas
  * Usar comandos dockers no CLI - Interface de linha de comando;
  * Criar um contêiner Docker para uma aplicação de front-end;
  * Criar um contêiner Docker para uma aplicação de back-end;
  * Criar um contêiner Docker para uma aplicação de testes;
  * Orquestrar os três contêineres utilizando o Docker compose.

---
# Requisitos desenvolvidos no projeto
## Requisitos Obrigatórios:

- ✅ 1. Crie um novo container de modo interativo sem roda-lo nomeando-o como `01container` e utilizando a imagem `alpine` usando a versão `3.12`.
- ✅ 2. Inicie o container `01container`.
- ✅ 3. Liste os containers filtrando pelo nome `01container`
- ✅ 4. Execute o comando `cat /etc/os-release` no container `01container` sem se acoplar a ele.
- ✅ 5. Remova o container `01container` que está em andamento.
- ✅ 6. Faça o download da imagem `nginx` com a versão `1.21.3-alpine` sem criar ou rodar um container.
- ✅ 7. Rode um novo container com a imagem  `nginx` com a versão `1.21.3-alpine` em segundo plano nomeando-o como `02images` e mapeando sua porta padrão de acesso para porta `3000` do sistema hospedeiro.
- ✅ 8. Pare o container `02images` que está em andamento.
- ✅ 9. Gere uma build a partir do Dockerfile do `back-end` do `todo-app` nomeando a imagem para `todobackend`.
- ✅ 10.Gere uma build a partir do Dockerfile do `front-end` do `todo-app` nomeando a imagem para `todofrontend`.
- ✅ 11.Gere uma build a partir do Dockerfile dos `testes` do `todo-app` nomeando a imagem para `todotests`.
## Requisito Opcional:

- ❌ 12. Suba uma orquestração em segundo plano com o docker-compose de forma que `backend`, `frontend` e `tests` consigam se comunicar.

# Sobre os testes

O avaliador cria um **container especial** para executar a avaliação de `comandos`, `Dockerfiles` e `docker-compose`. 

Esse container é temporário, por tanto, ao começar ou terminar os testes locais, o avaliador remove automaticamente esse mesmo container, assim como seu volume associado.

O volume desse container, mapeia a pasta `./docker/` do seu projeto, para dentro dele, ou seja, a raiz desse container vai conter as pastas `./docker-commands/`, `./todo-app/` e seu arquivo `./docker-compose.yml`, quando estiver pronto.

Isso significa, que se pudessemos olhar para dentro do container de avaliação, veriamos a seguinte estrutura:

```bash
.
├── docker-commands
└── todo-app
    ├── back-end
    │   └── *
    ├── front-end
    │   └── *
    └── tests
        └── *
```

Por tanto, é importante entender que os comandos docker escritos em `command*.dc` estarão rodando dentro desse container especial (e não a partir da raiz do projeto, como em projetos anteriores).

---


# O que foi desenvolvido

O objetivo do projeto era "conteinerizar" as aplicações de frontend, backend e testes, criar uma conexão entre elas e orquestrar seu funcionamento.
# Execução de testes unitários

⚠ **É necessário ter o Docker instalado corretamente na sua máquina para rodar os testes locais**

Todos os requisitos do projeto serão testados automaticamente por meio do Jest. Basta executar o comando abaixo:

```bash
npm test
```

Você pode rodar um arquivo de `test` por vez, exemplo:

```bash
npm test nomedocontainer
```
⚠ **Atenção:** ⚠
Não  utilize a função `.only` ou `.skip` após o describe.

---