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

