## 初期化
```
List<String> list = new ArrayList<String>();  
List<String> list = new ArrayList<String>(Arrays.asList("要素１", "要素２"));  
List<String> list = new ArrayList<String>(){  
  {  
    add("要素１");  
    add("要素２");  
  }  
};  
```  
  
## 要素の削除  
```  
List<String> list = new ArrayList<String>(){  
  {  
    add("red");  
    add("white");  
    add("blue");  
  }  
};  
  
// red以外が削除  
list.removeIf(str -> str.length > 3);  
```  
