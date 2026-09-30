# java-week2-mini3
迷你 compiler：三個整數的加法敘述轉成 Mini-3 assembly

## OnlineGDB 執行與輸入方式
在 OnlineGDB 選擇 Java 執行 TinyCompiler.java 執行後，在輸入區輸入三個整數的加法敘述

## 測試資料
int result = 2 + 4 + 6 ；

## 執行結果
MOVI R1, 2
MOVI R2, 4
ADD R0, R1, R2
MOVI R2, 6
ADD R0, R0, R2
STORE [0], R0

## 問題一
第一次 ADD 之後，為什麼能用第三個整數覆蓋 R2 ？
R1 和 R2 的數值已經相加並存到 R0 ，可以把第三個整數放到 R2
## 問題二 
若輸入改成 int result=7+3+1; ，目前程式為什麼無法按預期讀取？
和程式原本使用 next()、nextInt() 讀取格式不同，沒有空白時，會被當成同一段資料
