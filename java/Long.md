## Long型　→　String型への変換  
nullを考慮して、引数２つのObjects.toString()を利用する。  
LongのtoStringでも変換可能だが、nullだと落ちる。  
```  
Long long = 10L  
String  res = Objects.toString(long, "");  
```  
