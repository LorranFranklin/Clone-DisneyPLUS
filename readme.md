# Criando Clone do Disney Plus

## 1 - Primeiro criamos o repositório no gitHub

## 2 - Iniciamos o Git e clonamos o repositório do gitHub na pasta de nosso projeto.

## 3 - Iniciamos o projeto com `npm init --yes` assim vai pular todas as pergutas de configurações

## 4 - Instalamos o gulp e o gulp-sass como comando `npm install --save-dev gulp gulp-sass`

## 5 - Criamos a pasta `.gitignore` e adcionamos as pastas que queremos que o `git ignore`

## 6 - Criação do arquivo `gulpFile.js`

## 7 - criando `function test` no arquivo `gulpFile`

## 8 - iniciando a function no terminal `gulp` este por sua vez irá apresentar um erro, por conta que a pasta do gulp em `node_modules` não consegue ser localizada pelo windows. para isso iremos:

## 9 - Criar `script` no `package.json`

```
  "scripts": {
    "build": "gulp",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```

## 10 - Rodando o comando `npm run build`

## 11 - Resultado

```
npm run build

> clone-disney-plus@1.0.0 build
> gulp

[20:19:19] Using gulpfile ~\OneDrive\Área de Trabalho\CLONE-DISNEY-PLUS\gulpfile.js
[20:19:19] Starting 'default'...
Olá Lorran!
[20:19:19] Finished 'default' after 1.87 ms
```

## 12 - Function gulpFile:

```
function testGulp(cb) {
  console.log("Olá Lorran!")
  cb();
}

exports.default = testGulp;
```

## 13 - Instalando o `SASS` `npm install --save-dev sass`

## 14 - configurar o SASS

## 15 - Add imagens

## 16 - instalando puglin `npm install --save-dev gulp-imagemin@7.1.0` que irá utilizar as imagens na pasta dist minimizando às

## 17 - Criar e organizar function images

```
function images() {
  return gulp
    .src('./src/images/**/*')
    .pipe(imagemin())
    .pipe(gulp.dest('./dist/images'));
}

exports.default = gulp.parallel(styles, images);

exports.watch = function () {
  gulp.watch('./src/styles/*.scss', gulp.parallel(styles));
};
```

## 18 - Criar import

```
const imagemin = require('gulp-imagemin');
```

## 19 - Trabalhar no arquivo `.scss`

## 20 - Estaremos utilizando a `metodologia BEM` teremos aqui, o elemento `.text` e o modificador `--small` veja abaixo

```
.text--small {
  @include text(12px);
}
```

## 21 - Configurando watch

```
 "scripts": {
    "dev": "gulp watch",
    "build": "gulp",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```
## Instalando gulp na versão 4.0.2 ```npm install --sav-dev gulp@4.0.2```