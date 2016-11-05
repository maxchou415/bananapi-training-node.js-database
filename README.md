# BananaPi M2+ Training Nov. 5

## Introduction
本 Project 主要是以 Node.js + MongoDB with APi design 的部分。

## How to do?

### Step 1 - 抓下本專案
開啟您指定的路徑下終端機，在終端機內輸入
（以下全部步驟皆在 終端機 內部執行）
<br>
```git clone https://github.com/maxyihsunchou/bananapi-training-node.js-database.git```

### Step 2 - 進入專案資料夾
```cd bananapi-training-node.js-database```

### Step 3 - 安裝 Node.js 與 MongoDB
#### 安裝 Node.js 與 NPM
<br>
```sudo apt-get update```
<br>
#### Node.js
<br>
```sudo apt-get install nodejs```
<br>
#### NPM
<br>
```sudo apt-get install npm```
<br>
#### MongoDB
<br>
```sudo apt-get install -y mongodb```
<br>
### Config MongoDB
<br>
```sudo vim /lib/systemd/system/mongod.service```
<br>
在此檔案內貼上以下文字
<br>
```
[Unit]
Description=High-performance, schema-free document-oriented database
After=network.target
Documentation=https://docs.mongodb.org/manual

[Service]
User=mongodb
Group=mongodb
ExecStart=/usr/bin/mongod --quiet --config /etc/mongod.conf

[Install]
WantedBy=multi-user.target
```
<br>
按ESC 之後以 ```:wq``` 儲存變更
<br>
#### 請確任全部動作安裝都執行過
<br>
在目錄裡下輸入
```sudo service mongod start```
<br>
開啟 MongoDB 的服務
<br>
與
<br>
```npm start```
