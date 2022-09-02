# Gerador de parcela
Gerador de parcela. Gere parcelas facimente, facilite o desenvolvimento utilizando para gerar por exemplo mensalidade, repasse, vendas entre outras ações.


Para começar clone o repositório com o comando.
```
git clone https://github.com/gleissonneves/gerador-de-parcela.git

```
ou click no [link aqui](https://github.com/gleissonneves/gerador-de-parcela/archive/main.zip)

Se preferir faça a instalação usando o [npm](https://www.npmjs.com/package/gerador-de-parcela).

### Importe o Gerador de parcela no HTML

No HTML requisite o script.

```html
<body>
  <script>
    const resource = require('gerador-de-parcela');
    let datas = resource.generateDate(23, 11, 2022, 12)
    let parcel = resource.generateParcel(datas, 'R$: 200.00')
    
    console.log(datas, parcel);  
  </script>
</body>
 ```
  
 ### Instância a função de datas
 
 A função responsável por gerar a(s) data(s) para compor a(s) parcela(s)
 necessita de algumas informações para parametrizar.
```
generateDate(day, month, year, looping)
 
day recebe o dia;
month representa a quantidade de messes;
year representa o ano recorrente;
looping representa a quantidade de meses que será gerado a(s) data(s).
```
 
```html
<body>
    <script>
      // Example:
      const resource = require('gerador-de-parcela');
      let datas = resource.generateDate(23, 11, 2022, 12)
    </script>
</body>
```

 ### Instância a função de Gera Parcelas
 
 A função responsável por gerar a(s) parcelas(s) de fato onde dizemos a ela
 os dias das parcelas.
 
```
generateParcel(arrDate, valueParcel)
 
arrDate recebe um array de data(s) que nos devolve
indice, o valor da(s) parcela(s), a data e o status que por padrão é "Em aberto";

valueParcel é o valor padrão de finido da parcela.
```
 
```html
<body>
    <script src="./generateParcel.js"></script>
    <script>
      // Example:
      const resource = require('gerador-de-parcela');

      // gera uma parcela única para o data '01-01-1999'
      let parcelSingle = test.generateParcel(['01-01-1999'], 'R$: 200.00')

      // gera parcelas durante o periodo de 5 anos, sendo a data de pagamento todo dia 23 começando a partir do mês 11 do ano de 2022
      let fiveYears = 12 * 5;

      let datas = resource.generateDate(23, 11, 2022, fiveYears);
      let parcel = resource.generateParcel(datas, 'R$: 200.00');
    </script>
</body>
```
  
  
#### Aquela espiadinha

Para deixar a mostra os dados devemos utilizar o console já que
ele nos permite ver as propriedades, volores de objetos, Arrays entre outros elementos.

## Licença
Este projeto esta sobe a licença MIT.

Feito com :heart: por Gleisson Neves 👋🏽
