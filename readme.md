## Criando Clone do Disney Plus

1 - Primeiro criamos o repositório no gitHub
2 - Iniciamos o Git e clonamos o repositório do giHub na pasta de nosso projeto.
3 - Iniciamos o projeto com `npm init --yes` assim vai pular todas as pergutas de configurações
4 - Instalamos o gul e o gulp-sass como comando `npm install --save-dev gulp gulp-sass`
5 - Criamos a pasta `.gitignore` e adcionamos as pastas que queremos que o `git ignore`
6 - Criação do arquivo `gulpFile.js`
7 - criando function test no arquivo gulpFile
8 - iniciando a function no terminal `gulp` este por sua vez irá apresentar um erro, por conta que a pasta do gulp em node moidules não consegue ser localizada pelo windows. para isso iremos:
9 - Criando `script` no `package.json`

```
  "scripts": {
    "build": "gulp",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```
10 - Rodando o comando ```npm run build```
11 - Resultado
```
npm run build

> clone-disney-plus@1.0.0 build
> gulp

[20:19:19] Using gulpfile ~\OneDrive\Área de Trabalho\CLONE-DISNEY-PLUS\gulpfile.js
[20:19:19] Starting 'default'...
Olá Lorran!
[20:19:19] Finished 'default' after 1.87 ms
```

12 - Function gulpFile:
```
function testGulp(cb) {
  console.log("Olá Lorran!")
  cb();
}

exports.default = testGulp;
```

13 - Instalando o ```SASS``` ```npm install --save-dev sass```
14 - configurar o SASS