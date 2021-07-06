# Backend com NodeJs e Express 


<p align="center">
 <img width="200px" src="https://user-images.githubusercontent.com/85380530/124514592-c6da1e80-ddb3-11eb-864b-d8c3beb092a5.PNG" />
</p>


[![NPM](https://img.shields.io/npm/l/react)](https://github.com/rodrigoxsantos/bootcamp/blob/main/LICENSE) 

## 🖥️ Sobre o projeto 
> Nesta aplicação você descobrirá como construir um servidor web utilizando NodeJs e Express .
> 
# 📝 Introdução

> ## Configurando ambiente
> Acesse o site do NodeJS e faça o download da versão LTS mais atualizada e que
corresponda ao seu sistema operacional, você pode acessar o material através deste link [oceanbrasil.com](http://cms.oceanbrasil.com:8001/uploads/guest/9bc063513c-ocean-preparacao-trilha-backend.pdf), Faça a instalação do software seguindo as opções padrão.
Caso você esteja no Windows, o software npm (node package manager) também
será instalado.
Caso você esteja no Linux, pode ser necessário instalar o npm separadamente.

# 📝 Criando um projeto ``NodeJs``

> Crie uma pasta em sua máquina, ou através do terminal utilizando o seguinte comando no (Windows e no Linux)para criar a pasta:

```bash
mkdir nome-que-desejar
```
 <img width="200px" src="https://user-images.githubusercontent.com/85380530/124524850-10863180-ddd3-11eb-8bd6-964b842aab0a.PNG" />
 
 > Abre o Terminal (no Windows, abra o prompt da linha de comando dentro da pasta de seu projeto).
 
 <img width="200px" src="https://user-images.githubusercontent.com/85380530/124525270-0b29e680-ddd5-11eb-9492-770e613f9257.PNG" />

> Ou, através do terminal acesse a pasta que você criou navegue até seu diretório através do comando ``` cd nome-da-pasta/, ``` o terminal indica a pasta que você está atualmente, basta se deslocar até o diretório desejado digitando o nome da pasta do seu projeto.

```bash
cd introducao-backend-ocean/
```

> Segue um exemplo:

 <img width="400px" src="https://user-images.githubusercontent.com/85380530/124526025-d4a19b00-ddd7-11eb-8ead-cabbc451af6d.PNG" />


> Use o editor de texto de sua preferência ( estou usando Visual Studio Code).

 <img width="400px" src="https://user-images.githubusercontent.com/85380530/124526318-d3bd3900-ddd8-11eb-85be-a9a5496c79d1.PNG" />

> Para adentrar no visual studio através do terminal já dentro da pasta do seu projeto, basta digitar o comando a seguir.
> 
```bash
 code .
```
> Exemplo: 
> 
<img width="550px" src="https://user-images.githubusercontent.com/85380530/124527130-2992e080-dddb-11eb-9feb-ca2e5555a56c.PNG" />

# 📝 Configurando o arquivo ```package.json```

> Agora vamos gerar o arquivo com as configurações iniciais de nossa aplicação (package.json).

> Para obter mais informações sobre como o package.json funciona, consulte Detalhes do tratamento de [docs.npmjs.com](https://docs.npmjs.com/cli/v7/configuring-npm/package-json).
> 
> Já dentro de sua pasta, digite:

```bash
npm init -y
```
<img width="400px" src="https://user-images.githubusercontent.com/85380530/124529123-35cd6c80-dde0-11eb-8296-0e33a660d286.PNG" />

> Arquivo de dependências do projeto gerado.
> 
<img width="300px" src="https://user-images.githubusercontent.com/85380530/124609923-73fd7700-de46-11eb-940a-1679e8127a13.PNG" />

# 📝 Criando um arquivo ```index.js ```
> Através de seu editor de texto, crie o arquivo index.js. Neste arquivo ficará a parte principal do código, ou seja, é nele que programaremos as funcionalidades da nossa aplicação.

 <img width="400px" src="https://user-images.githubusercontent.com/85380530/124527773-ca35d000-dddc-11eb-8814-8e46ee00451a.PNG" />

> Dentro deste aquivo digite o código a seguir:
 
```bash
console.log("Wello, Word!");
```
<img width="300px" src="https://user-images.githubusercontent.com/85380530/124640373-b1bcc880-de63-11eb-8dda-4e3d83475f16.PNG" />

> Salve o arquivo na pasta que você criou.

Por último, vá no terminal e digite o comando a seguir:
```bash
node index.js
```
> Resultado em seu terminal:

 <img width="400px" src="https://user-images.githubusercontent.com/85380530/124529889-d708f280-dde1-11eb-9142-9ea6728c5ee5.PNG" />
 
 
> ## <p align="center">Antes da instalação do Express realizei a configuração do Nodemon na aplicação, comandos a seguir:</p>
 
 
 # 📝 Configurando ``Nodemon`` na aplicação

> Nodemon é uma ferramenta que ajuda a desenvolver aplicativos baseados em node.js, reiniciando automaticamente o aplicativo de nó quando mudanças de arquivo no diretório são detectadas.
Para obter mais informações sobre como o nodemon funciona, consulte detalhes do tratamento em [developer.mozilla.org](https://developer.mozilla.org/pt-BR/docs/Learn/Server-side/Express_Nodejs/Introduction).

## Instalação
> Usando o npm (a forma recomendada): [www.npmjs.com](https://www.npmjs.com/package/nodemon).
> 
> ```bash npm install -g nodemon ```
> 
> Após a instalação do arquivo , você irá editar seu package.json no campo scripts  assumindo que a index.js iniciaria o aplicativo, podemos criar um script dev, que irá recarregar nosso aplicativo nas mudanças de arquivo durante o desenvolvimento.
> 
> Para criar um script dev, adicione uma nova "dev"entrada no campo de scripts em package.json.
```bash
"scripts": {
    "start": "node index",
    "dev": "nodemon index"
  },
  ```
 <img width="400px" src="https://user-images.githubusercontent.com/85380530/124543148-1a238f80-ddfb-11eb-99c2-7984c5522fe7.PNG" />
 
  > Agora executo a minha aplicação através do comando:
 >  ``` npm run dev ```
 >  
  > Geralmente, 'dev' especifica o uso de desenvolvimento  ```( npm run dev )  ```
 
 


 
 # 📝 Introduzindo o Express
 
 > ### Instalação
> Antes de instalar, baixe e instale Node.js . Node.js 0.10 ou superior é necessário a instalação é feita usando o ```npm install``` comando :
```$ npm install express```,
> para obter mais informações, acesse o guia de instalação [expressjs.com/en/starter](http://expressjs.com/en/starter/installing.html).
 
 > ## Criação de um servidor expresso
 
> Para obter mais informações sobre como o Express funciona, consulte detalhes em [developer.mozilla.org](https://developer.mozilla.org/pt-BR/docs/Learn/Server-side/Express_Nodejs/Introduction).
 
> Com o Node e Express instalados, crie um novo ```index.js```arquivo e abra-o com seu editor de código. Em seguida, adicione as seguintes linhas de código:

> index.js 
```bash 
const express = require('express');

const app = express();
```

> #### Explicação do código: 
> A primeira linha aqui é pegar o módulo Express principal do pacote que você instalou. Este módulo é uma função, que então executamos na segunda linha para criar nossa ```app ```variável. Você pode criar vários aplicativos dessa forma, cada um com suas próprias solicitações e respostas.


> index.js
```bash 
const express = require('express');

const app = express();

app.get('/', (req, res) => {
  res.send('Successful response.');
});
```
> #### Explicação do código: 
> É nessas linhas de código que informamos ao nosso servidor Express como lidar com uma ```GET```solicitação para o nosso servidor. Express inclui funções semelhantes para ```POST, PUTetc```. usando ```app.post(...), app.put(...)etc```.

> Essas funções têm dois parâmetros principais. O primeiro é o URL para esta função agir. Neste caso, estamos almejando ```'/'```, que é a raiz do nosso site: neste caso ```localhost:3000,```.

> O segundo parâmetro é uma função com dois argumentos:, ```reqe res```. ```req```representa a solicitação enviada ao servidor; Podemos usar esse objeto para ler dados sobre o que o cliente está solicitando fazer. resrepresenta a resposta que enviaremos de volta ao cliente.

> #### Explicação do código: 
> Aqui, nós estamos chamando uma função em ```res``` para enviar de volta uma resposta: ```'Successful response.'```.

> index.js
```bash 
const express = require('express');

const app = express();

app.get('/', (req, res) => {
  res.send('Successful response.');
});

app.listen(3000, () => console.log('Example app is listening on port 3000.'));

```
> Finalmente, uma vez que configuramos nossas solicitações, devemos iniciar nosso servidor! Estamos passando ```3000```para a ```listen```função, que informa ao aplicativo em qual porta escutar. A função passada como o segundo parâmetro é opcional e é executada quando o servidor é inicializado. Isso nos fornece algum feedback no console para saber se nosso aplicativo está em execução.
> 
> Vá a janela do terminal e execute seu aplicativo com o comando:
> 
> ``` node index.js```
>
> Em seguida, visite localhost:3000 em seu navegador da web, a janela do seu navegador irá exibir: ``` 'Successful response'. ```
> 
<img width="600px" src="https://user-images.githubusercontent.com/85380530/124654026-65c64f80-de74-11eb-9e5e-794ca2d8f57d.PNG" />


> Sua janela de terminal irá mostrar: ``` 'Example app is listening on port 3000.```
> 
 <img width="600px" src="https://user-images.githubusercontent.com/85380530/124653922-47605400-de74-11eb-8280-f87563c33c42.PNG" />
 
 > E aí está, um servidor web! 
 > ## ✨ Tecnologias utilizadas

> ### Beck end
> - JavaScript 

 > ## 👨🏽‍💻 Autor
 > 
Rodrigo Xavier dos Santos
>
[Linkedin](https://www.linkedin.com/in/rodrigoxsantos/) 
 
 

