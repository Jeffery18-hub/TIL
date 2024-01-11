## Function Declaration

Function hoist:  you can init before the declaration

```js
function func(name){
    console.log(name);
}
```

## Function Expression

No hoist

```js
var func = function(name){
    console.log(name);
}
```