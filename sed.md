# sed

## include at beginning of each line

The following command will add "'" to the beginning of each line.

```
sed "s/^/'/" old.txt  > new.txt
```

## include at end of each line

The following command will add "'," to the end of each line.

```
sed "s/$/',/" old.txt > new.txt
```