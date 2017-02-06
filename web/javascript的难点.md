```javascript
function Animal (name){
    this.name = name;
};

Animal.prototype.getName = function(){
    return this.name;
}
Animal.prototype.eat =function(food){
    console.log(this.name,' eat:',food)

}

function Ferret (){
};
Ferret.prototype = new Animal('tobi')

Ferret.prototype.type = 'domestic'

Ferret.prototype.eat = function(food){
    Animal.prototype.eat.call(this,food)
    console.log(this)
    Animal.prototype.eat(food)

}

var f = new Ferret()
f.eat('a')
```
