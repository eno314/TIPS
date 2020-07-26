# Python dictionary tips

## 最大値・最小値を取得

### keyの最大値・最小値を取得

```:python
>>> dict = {'a': 0, 'b': 1}
>>> max(dict)
'b'
>>> min(dict)
'a'
```

### valueの最大値・最小値を取得

```:python
>>> dict = {'a': 0, 'b': 1}
>>> max(dict.values())
1
>>> min(dict.values())
0
```

### 最大値・最小値のvalueを持つkeyを取得

```:python
>>> dict = {'a': 0, 'b': 1}
>>> max(dict, key=dict.get)
'b'
>>> min(dict, key=dict.get)
'a'
```

## 内包表記で辞書を作る

```:python
>>> dict = {key: 0 for key in "abcdedg"}
>>> dict
{'a': 0, 'b': 0, 'c': 0, 'd': 0, 'e': 0, 'g': 0}
```

## 辞書の要素を削除する

### 1件だけ削除

```:python
>>> dict = {'a': 0, 'b': 1}
>>> del dict['a']
>>> dict
{'b': 1}
```

### 全削除

```:python
>>> dict = {'a': 0, 'b': 1}
>>> dict.clear()
>>> dict
{}
```

### 値を取得して削除

```:python
>>> dict = {'a': 0, 'b': 1}
>>> a_value = dict.pop('a')
>>> dict
{'b': 1}
>>> a_value
0
```

### ランダムにキーと値を取得しつつ、その要素を削除

```:python
>>> dict = {'a': 0, 'b': 1}
>>> key, value = dict.popitem()
>>> dict
{'a': 0}
>>> key, value
('b', 1)
```
