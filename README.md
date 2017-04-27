# Grid Flexivel e Sugestão de estrutura de pastas

Segue abaixo como usar o grid e a estrutura da pasta usada.

## Estrutura das pastas

```
.root or theme project
├── gulp/
|	├── node_modules/
|	├── tasks/
|	|	├── clone-file.js
|	|	├── concat-min-js.js
|	|	├── sass.js	'converte o sass para css e minifica'
|	|	└── watch.js
|	|
|	├── Gulpfile.js
|	└── package.json
|
├── src/
|   ├── css/
|   ├── fonts/	'esta pasta será clonada com o gulp'
|   ├── js/
|   └── sass/
|
├── static/
|   ├── css/	'receberá o arquivo minificado'
|   ├── fonts/	'esta pasta foi clonada da pasta src com o gulp'
|   ├── js/		'receberá o arquivo minificado'
|   └── images/
|									
├── .gitignore	
└── README.md
```