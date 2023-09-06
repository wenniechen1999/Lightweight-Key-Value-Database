# 💾 NewSQL-Engine 
## 輕量級鍵值型資料庫
NewSQL 是對各種新的可拓展、高性能資料庫的簡稱，不僅具有NoSQL對大量數據存儲管理能力，也保留傳統資料庫支持ACID和SQL等特性。其中，redis核心資料結構就是使用 [跳表(Skip List)](https://en.wikipedia.org/wiki/Skip_list) 這種數據結構來實現高效的數據存儲和查詢。

這個輕量級鍵值型資料庫使用了C++實現跳表結構，並且具有以下功能：

1. 插入 (insert)
2. 刪除 (delete)
3. 查詢數據 (search)
4. 數據展示 (display)
5. 數據落盤 (dump)
6. 文件載入數據 (load)
7. 顯示資料庫大小 (size)

## 📁 資料夾與主要檔案
* 🗂️ sklist / skiplist.h：實現存儲的核心功能
* 🗂️ stress-test / stress_test.cpp：壓力測試
* 🗂️ bin ： 生成可執行文件目錄 `.main` , `.stress`
* 🗂️ store：數據落盤的文件夾，存放 `dumpFile` , `dump`
* makefile：編譯腳本
* main.cpp：主程式
* stress_test_start.sh：壓力測試腳本
* README.md ： 介紹與使用說明
 

## ▶️ 運行方式
### 主程式
在terminal運行以下指令

1. `make`				
complie main.cpp

2. `./bin/main 10`		
10為最大跳表樹高，可以自己更改數字（上限為16）

### 壓力測試
 `sh stress_test_start.sh` 		
運行腳本來測試輕量級鍵值型資料庫性能

## 存儲引擎表現
### 插入
每秒查詢率(QPS)：23.61w
### 取數據
每秒查詢率(QPS)：18.66w







