# Grid Flexivel e Sugestão de estrutura de pastas

Esse grid é uma versão melhorada do Bootstrap, pois senti a necessidade de outros breakpoints. Esse grid é feito com Mixins.
Segue abaixo como usar o grid e a estrutura da pasta usada para organizar os arquivos do sass.

## Estrutura das pastas

```
.src

├── sass/
|   ├── helpers/
|   |    |
|   |    ├── mixins/
|   |    |   └── _grid.scss
|   |    |
|   |	 └── _mixins.scss
|   |
|   ├── layout/
|   |    └── _grid.scss
|   |
|   └── all.scss
|									
├── .gitignore	
└── README.md
```

## Como usar o GRID

```
.nome_da_classe {
	@include make-grid-column($columns, $breakpoint: $break-point-default, $gutter: $grid-gutter-width);
}

```

## Explicação do mixin make-grid-column

```
1. Variável $columns
	Quantidade de colunas a serem utilizadas. Máximo de 12 colunas, porque esta configurada essa quantidade no arquivo '_variable_grid.scss'.
```

```
2. Variável $breakpoint
	O próprio nome já diz. Digite o ponto aonde terá a alteração de como será o comportamento da DIV. Caso não informe o valor, por default o breakpoint começará com o valor '0', pois é o valor setado na variável $break-point-default que se encontra no arquivo '_variable_grid.scss'.
```

```
3. Variável $gutter
	O parâmetro que essa variável receber irá alterar o espaçamento das laterais da coluna. Caso não sete algum valor por padrão ela terá 15px, se quiser alterar acesse o arquivo '_variable_grid.scss'.
```
