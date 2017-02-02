
tutorial http://osherove.com/tdd-kata-1/


Libros interesantes:
- TDD by example - kent beck
- Clean code



Web para practicar http://tddbin.com


```javascript
describe('StringCalculator', function() {

  it('simple values equal?', function() {
    assert.equal(0, add(""));
  });

    it('simple values equal?', function() {
    assert.equal(1, add("1"));
  });

      it('simple values equal?', function() {
    assert.equal(3, add("1,2"));
  });

      it('simple values equal?', function() {
    assert.equal(9, add("1,2,6"));
  });

});

  describe('Sumar con saltos de linea', function() {
        it('simple values equal?', function() {
    assert.equal(6, add("1\n2,3"));
  });



});

function add(string) {


  var array = string.split(',');

    return array
    .map( (elem) => {

    })
    .map( (elem) => {
    if (elem == "")
      return 0;
    return parseInt(elem);
  })
  .reduce((a,b) => a+b, 0);
}
```
