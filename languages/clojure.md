# Clojure

## (or) and (and)

_or_ returns either the first truthy value or the last value. 

_and_ returns the first falsey value or, if no values are falsey, the last truthy value.

# :keywords

Keywords can be used as functions that look up the corresponding value in a data structure

```clojure
> (def mymap 
    {:hello "world"})
> (:hello mymap)
; => "world"
```

# documentation

There is a function for it, simply do 
```clojure
> (doc map)
```

and start reading about things.

# Defining Functions

```clojure
> (defn tubli 
    "makes everyone tubli"
    [name]
    (str name " on tubli!"))
> (tubli "Lars")
```


