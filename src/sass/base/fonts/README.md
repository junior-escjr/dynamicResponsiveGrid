#Adicionar o arquivo .scss chamando os arquivos da fonte. 
Ex:

```html
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../fonts/glyphicons-halflings-regular.eot');
  src: url('../fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'),
       url('../fonts/glyphicons-halflings-regular.woff') format('woff'),
       url('../fonts/glyphicons-halflings-regular.woff2') format('woff2'),
       url('../fonts/glyphicons-halflings-regular.ttf') format('truetype'),
       url('../fonts/glyphicons-halflings-regular.svg#Glyphicons Halflings') format('svg');

  font-weight: normal;
  font-style: normal;
}
```