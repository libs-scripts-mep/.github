# Bibliotecas de Script do M&P

## npm

[npm - Node Package Manager](https://www.npmjs.com/), atual versionador de pacotes do M&P, é responsável por gerenciar os pacotes das bibliotecas contidas nessa organização.

Através dele é possível:

- Criar e publicar pacotes
- Realizar download dos pacotes
- Auditar pacotes já instalados (Verifica integridade)
- Versionar pacotes já publicados
- Atualizar pacotes nos scripts

> ⚠️ Necessita node.js instalado na máquina para o CLI do npm funcionar. [Faça o download aqui.](https://nodejs.org/en/download/)


### Criando um novo pacote

Após realizar o primeiro commit do seu novo pacote npm, abra o terminal e rode o comando abaixo para inicializar o npm no repositório.

```npm init --scope=libs-scripts-mep```

A opção ```--scope``` determina a organização a qual o pacote pertence.

### Publicando pela primeira vez um pacote

```npm publish --access public```

Versionando e publicando uma nova versão de um pacote

