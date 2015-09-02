---
layout: post
title: Pyhton Environment Setup
author: "Mitch"
tags: Python
---

因最近重新開始學習研究 Python 

藉此文把開發環境的安裝步驟紀錄下來，方便以後查詢

* * *

* 安裝 Homebrew: 打開 Terminal > 將下列指令貼上執行

  ```
  ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  ```

* 透過 Homebrew 安裝 Python: Homebrew 會同時幫你安裝 Setuptools 及 pip

  ```
  $ brew install python
  ```

* 透過 pip 安裝 virtualenv

  ```
  $ pip install virtualenv
  ```

* 透過 pip 安裝 virtualenvwrapper (一定要先安裝好 virtualenv)

  ```
  $ pip install virtualenvwrapper
  ```

* 建立修改系統的 .bash_profile

  * 打開 Terminal, 輸入以下指令
  
    ```
    $ touch ~/.bash_profile; open ~/.bash_profile
    ```
  
  * 將以下的環境變數設定貼至檔案中並儲存

    ```
    export WORKON_HOME=~/Envs
    source /usr/local/bin/virtualenvwrapper.sh
    ```

* Virtualenv 的基本使用方法

  * 創建一個新的 virtual environment
  
    ```
    $ mkvirtualenv django18
    ```
  
  * 進入指定的 virtual environment
  
    ```
    $ workon django18
    ```
  
  * 跳出 virtual environment
  
    ```
    $ deactivate
    ```
  
  * 移除指定的 virtual environment
  
    ```
    $ rmvirtualenv django18
    ```

參考文章：

[Installing Python on Mac OS X](http://docs.python-guide.org/en/latest/starting/install/osx/)

[Virtual Environments](http://docs.python-guide.org/en/latest/dev/virtualenvs/)

[Mac OS X 如何更改系統路徑與環境變數](http://edscb.blogspot.tw/2014/02/mac-osx.html)