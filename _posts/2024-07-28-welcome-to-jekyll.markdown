---
layout: post
title:  "Pythonで自動化スクリプトを作成する方法"
date:   2024-07-28 16:06:49 +0900
categories: python automation
---
Pythonを使用して日常のタスクを自動化する方法を紹介します。以下は簡単な例です：

{% highlight python %}
import os

def organize_files(directory):
    for filename in os.listdir(directory):
        name, extension = os.path.splitext(filename)
        extension = extension[1:]
        
        if os.path.exists(os.path.join(directory, extension)):
            os.rename(os.path.join(directory, filename
