# Bibliotecas de Script do M&P

- [Bibliotecas de Script do M&P](#bibliotecas-de-script-do-mp)
- [npm](#npm)
  - [Criando usuário npm](#criando-usuário-npm)
  - [Fazendo login via CLI - Command-Line Interface](#fazendo-login-via-cli---command-line-interface)
  - [Instalando, desinstalando e atualizando pacotes](#instalando-desinstalando-e-atualizando-pacotes)
  - [Criando um novo pacote](#criando-um-novo-pacote)
  - [Publicando pela primeira vez um pacote](#publicando-pela-primeira-vez-um-pacote)
  - [Versionando e publicando um pacote](#versionando-e-publicando-um-pacote)

# npm

[npm - Node Package Manager](https://www.npmjs.com/), atual versionador de pacotes do M&P, é responsável por gerenciar os pacotes das bibliotecas contidas nessa organização.

Através dele é possível:

- Criar e publicar pacotes
- Realizar download dos pacotes
- Auditar pacotes já instalados (Verifica integridade)
- Versionar pacotes já publicados
- Atualizar pacotes nos scripts

> ⚠️ Necessita node.js instalado na máquina para o CLI do npm funcionar. [Faça o download aqui.](https://nodejs.org/en/download/)

## Criando usuário npm

Após realizar a instalação do [node.js](https://nodejs.org/en/download/), crie uma conta no [npm](https://www.npmjs.com/signup), e solicite acesso à organização [libs-scripts-mep](https://www.npmjs.com/org/libs-scripts-mep).

> ⚠️ Sugestão de nome visando padronização: inv-nome.sobrenome

## Fazendo login via CLI - Command-Line Interface

Com sua conta já criada, abra o terminal em qualquer repositório do sistema, e execute o comando ```npm adduser``` e siga as instruções de login.

## Instalando, desinstalando e atualizando pacotes

- Instalando:

No repositório do script, abra o terminal e execute o comando ```npm i @libs-scripts-mep/nome-do-pacote```.

Será criado em seu projeto uma pasta chamada ***node_modules*** contendo os pacotes instalados, e os arquivos ***package.json*** para gerenciar as versões de cada pacote.

A partir daí, basta incluir o caminho da biblioteca no ***.html*** do script com a tag 

```html
<script src="node_modules/@libs-scripts-mep/nome-do-pacote/nome-do-arquivo.js"></script>
```

>Cada pacote possui sua documentação própria

- Desinstalando:

No repositório do script, abra o terminal e execute o comando ```npm uninstall @libs-scripts-mep/nome-do-pacote```.

Esse comando removerá o registro do ***package.json***, e deletará a pasta do pacote em ***node_modules***

- Atualizando:

No repositório do script, abra o terminal e execute o comando ```npm update``` para atualizar todos os pacotes que possuem atualização.

> ⚠️ Certifique-se de que no ***package.json*** os pacotes tenham a notação ```^x.x.x``` afim de manter a compatibilidade.

## Criando um novo pacote

Após realizar o primeiro commit do seu novo pacote npm, no repositório do mesmo, abra o terminal e execute o comando: 

```npm init --scope=libs-scripts-mep```

O comando ```npm init``` irá inicializar o processo de registro, gerando ao fim, o arquivo ***package.json*** que contém as informações necessárias para publicar o pacote.

A opção ```--scope``` determina a organização a qual o pacote pertence, no caso, [libs-scripts-mep](https://www.npmjs.com/org/libs-scripts-mep).

## Publicando pela primeira vez um pacote

Ainda no repositório do pacote criado, execute o comando ```npm publish --access public``` para publicar no pacote.

Nesse momento, ele estará disponível em [libs-scripts-mep](https://www.npmjs.com/org/libs-scripts-mep).

## Versionando e publicando um pacote

Após realizar os commits das alterações na sua biblioteca, abra o terminal no repositório do pacote e execute o comando ```npm version x.x.x```, sendo ```x.x.x``` sua nova versão. O arquivo ***package.json*** será atualizado com a nova versão.

Em seguida execute o comando ```npm publish --access public``` para publicar a nova versão.

A partir desse momento, qualquer script que contenha esse pacote, se utilizado o comando ```npm update```, receberá a nova versão.