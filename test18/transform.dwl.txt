%dw 2.0
output application/json
---
((payload reduce ((env, obj={}) -> obj ++ env)) filterObject $ != "") distinctBy $

//distinctBy function takes the argument evaluates for each object and returns an unique values .whether it was having one or combination of others and for thius scrpt we get the unique values and reduce is used to transform an Array into any other type filterobject used to removes key:value pairs from Objects.