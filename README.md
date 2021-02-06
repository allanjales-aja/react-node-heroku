# react-node-heroku

-> Criar as pastas “Client” e “Server”;

-> sudo npm install -g express-generator;

-> npx create-react-app app1 na pasta "Client";

-> express na pasta "Server";

-> npm install na pasta "Server";

-> npm run build na pasta "app1";

-> sudo npm install -g serve;

-> Recortar a pasta build da pasta "Client" para a pasta "Server";

-> Acrescentar este código ao arquivo "app.js" da pasta "Server":

	app.use(express.static(path.join(__dirname, 'build')));

	app.get('/*', (req, res) => {  res.sendFile(path.join(__dirname, 'build', 'index.html'));
	});

-> npm start na pasta "Server";

-> http://localhost:3000/* no navegador;

-> Criar repositório no GitHub adicionando arquivos da pasta "Server" MENOS node_modules;

-> Heroku - Create new app - Deploy - Deployment method - GitHub;

-> Conectar repositório do GitHub;

-> Clicar em “Deploy Branch”;

-> Heroku vai instalar todos os módulos Node;

-> Clicar em “View” para visualizar o projeto.




Fonte: https://www.freecodecamp.org/news/deploy-a-react-node-app-to/
