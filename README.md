# Grid Flexivel e Sugestão de estrutura de pastas

Esse GRID foi pensado na necessidade que eu tive de utilizar outros breakpoints que o Bootstrap não oferece. Então eu estudei como funciona a estrutura do mixin do Bootstrap e aprimorei os aspectos da função do mixin para que me atenda a qualquer tipo de situação referente ao grid, com isso posso usar qualquer valor no meu breakpoint.

### Estrutura das pastas
O link abaixo é o repositório indicado para a utilização desse GRID, mas sem problemas caso não queira segui-lo.
- [Link para o repositório](https://github.com/junior-escjr/folderStructure)


## Como usar o GRID

- param int $columns [quantidade de colunas]
- param String $breakpoint [breakpoint. Ex. 777px]
- param String $gutter [espaçamento lateral. Ex. 30px]

```
@include make-grid-column($columns, $breakpoint, $gutter);
```

1 - Como usar na classe (no caso abaixo usando 6 colunas com a breakpoint e o espaçamento definidos ).

```
.nome_da_classe {
	@include make-grid-column(6);
}
```

Resultado:

```
.nome_da_classe {
	position: relative;
	min-height: 1px;
	padding-left: 7.5px;
	padding-right: 7.5px;
	float: left;
	width: 50%;
}
```

2 - Agora o exemplo abaixo estou utilizando a mesma função mais de uma vez na mesma classe, mas com breakpoints e quantidade de colunas diferentes. O primeiro o breakpoint começa a partir do zero, já o segundo a partir de 451px.

```
.nome_da_classe {
	@include make-grid-column(6);
	@include make-grid-column(8, 451px);
}
```

Resultado:

```
@media (min-width: 0) {
  	.nome_da_classe {
	    position: relative;
	    min-height: 1px;
	    padding-left: 7.5px;
	    padding-right: 7.5px;
	    float: left;
	    width: 50%;
	}
}

@media (min-width: 451px) {
  	.nome_da_classe {
	    position: relative;
	    min-height: 1px;
	    padding-left: 7.5px;
	    padding-right: 7.5px;
	    float: left;
	    width: 66.66667%;
	}
}

```
3 - No próximo exemplo vou utilizar todos os três parâmetros. O terceiro parâmetro altera a espaçamento das laterais da coluna.

```
.nome_da_classe {
	@include make-grid-column(10, 500px, 50px);
}
```

Resultado

```
.nome_da_classe {
    position: relative;
    min-height: 1px;
    padding-left: 25px;
    padding-right: 25px;
    float: left;
    width: 83.33333%;
}
```

## Como usar o GRID junto com o 'offset'

A forma que é usado o mixin 'offset' é igual ao mixin das colunas, a diferença que a função usa dois parâmetros ao invés de três.

```
@include make-grid-column-offset($columns, $breakpoint);
```


Utilizando o mixin do offset na classe acompanhado do mixin das colunas.

```
.nome_da_classe {
	@include make-grid-column(6);
	@include make-grid-column-offset(3);
}
```

Resultado do offset

```
.nome_da_classe {
    margin-left: 8.33333%;
}
```

Resultado da coluna

```
.nome_da_classe {
    position: relative;
    min-height: 1px;
    padding-left: 25px;
    padding-right: 25px;
    float: left;
    width: 83.33333%;
}
```