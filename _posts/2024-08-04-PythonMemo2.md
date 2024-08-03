---
layout: post
title: Python 備忘録 変数
date: 2024-08-04
category: プログラミング
tags: [Python, 基礎]
---

**論理・比較演算と条件分岐の基礎**

- **条件分岐 (if 文)**  
  条件に応じて異なる処理を実行するための構文。基本的な形式は次の通り：

  ```python
  if 条件:
      # 条件が True のときに実行されるコード
  else:
      # 条件が False のときに実行されるコード
  ```

  例：

  ```python
  def compare(a, b):
      if a > b:
          return a
      else:
          return b
  ```

  上記の `compare` 関数は、2つの引数のうち大きい方を返す。

- **比較演算子**  
  比較演算子を使って値を比較する。代表的なものは以下の通り：

  - `a < b`  : `a` が `b` より小さい
  - `a <= b` : `a` が `b` 以下
  - `a > b`  : `a` が `b` より大きい
  - `a >= b` : `a` が `b` 以上
  - `a == b` : `a` と `b` が等しい
  - `a != b` : `a` と `b` が異なる

- **論理演算子**  
  条件を組み合わせるための演算子。代表的なものは以下の通り：

  - `and`  : 両方の条件が True のとき True
  - `or`   : どちらかの条件が True のとき True
  - `not`  : 条件が False のとき True

  例：

  ```python
  def is_valid(i, j):
      return i >= 0 and j > 0
  ```

- **真理値**  
  条件式の結果が True または False である。例：

  ```python
  x = 3
  if x > 1:
      print("x は 1 より大きい")
  ```

  このコードでは `x > 1` が True であるため、メッセージが表示される。

- **オブジェクトと `None`**  
  Python の全ての値はオブジェクトであり、`None` は値が存在しないことを表す。`None` は条件式では False として扱われる。

  ```python
  def check_value(value):
      if value is None:
          print("値は None")
      else:
          print("値は None ではない")
  ```

  上記のコードでは、`value` が `None` であるかどうかをチェックする。

