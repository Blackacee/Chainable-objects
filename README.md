# Chainable-objects
 
function Vec(x = 0, y = 0){
 this.x = x;
 this.y = y;
 // the new keyword implicitly implies the return type
 // as this and thus is chainable by default.
}
Vec.prototype = {
 add : function(vec){
 this.x += vec.x;
 this.y += vec.y;
 return this; // return reference to self to allow chaining of function calls
 },
 scale : function(val){
 this.x *= val;
 this.y *= val;
 return this; // return reference to self to allow chaining of function calls
 },
 log :function(val){
 console.log(this.x + ' : ' + this.y);
 return this;
 },
 clone : function(){
 return new Vec(this.x,this.y);
