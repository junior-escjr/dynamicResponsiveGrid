# Grid Flexivel e Sugestão de estrutura de pastas

Esse grid é uma versão melhorada do Bootstrap, pois senti a necessidade de outros breakpoints. Esse grid é feito com Mixins.
Segue abaixo como usar o grid e a estrutura da pasta usada para organizar os arquivos do sass.

## Estrutura das pastas
O link abaixo é o repositório indicado para a utilização desse GRID, mas sem problema caso não queira segui-lo.
- [Link para o repositório](https://github.com/junior-escjr/folderStructure)


## Como usar o GRID

Exemplificando com as variáveis

```
@include make-grid-column($columns, $breakpoint, $gutter);

```

Como usar na classe (no caso abaixo usando 6 colunas com a breakpoint e o espaçamento default).

```
.nome_da_classe {
	@include make-grid-column(6);
}

```

Agora passando como parâmetro as colunas e o breakpoint.

```
.nome_da_classe {
	@include make-grid-column(6, 500px);
}

```

Agora passando como parâmetro as colunas, breakpoint e o espaçamento das laterais da coluna.

```
.nome_da_classe {
	@include make-grid-column(6, 500px, 50px);
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
