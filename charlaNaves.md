9-2-016
# Desarrollo e Integración continua + TDD - Test Driven Development

Empresa: Karumi   
Jorge Juan Barroso Carmona    
@flipper83

## Herramientas para diseñar
* Sketch
* zeplin   
* proto.io  
* invision
* mockinnbird!

Comportamiento creado PR

- Review guidelines
- Code smells
- Naming
- DRY
- Test quality
- Give positive feedback

Definir un glosario(Utilizar un lenguaje standard)  

Análisis estático   
CheckStyle -> Importante para mergear código

travis jenkins

## Belleza del código
* Naming


From STUPID to SOLID
STUPID
S =
T =
U =
P =
I = 
D = Duplicidad

S = Una entidad hace una cosa   
O =     
L =     
I =     
D =     

```javascript
describe('BasketCalculator', function() {

  it('ShouldReturnZeroWhenbasketIsEmpty', function() {
    var  books = [];
    assert.equal(0, calculatePrice(books));
  });

  it('ShouldReturnEigthWhenBasketHaveOneBooks', function() {
    var  books = [1];
    assert.equal(8, calculatePrice(books));
  });


  it('ShouldReturnPriceWhenbasketHaveTwoBooksSame', function() {
    var  books = [1,1];
    assert.equal(16, calculatePrice(books));
  });

  it('ShouldReturnPriceWhenbasketHaveThreeSameBooks', function() {
    var  books = [1,1,1];
    assert.equal(24, calculatePrice(books));
  });

  it('ShouldReturnPriceWhenbasketHaveTwoDiferentBooks', function() {
    var  books = [1,2];
    assert.equal(15.2, calculatePrice(books));
  });


});

function calculatePrice(books) {
  var discount = 0;
  if (books.length > 1) {
    if (books[0] != books[1]) {
      discount = .95;
    }
  }
  var price = books.length * 8;

  if (discount)
    price *= discount;

  return  price;
}

```
