# 基於檢索模型的客服自動回覆系統

# 這個專案在做什麼？

將使用者常提出的問題預先進行分類並設定好回答，當使用者輸入問題時自動判斷是哪一類型的問題並將答案回答給使用者。若出現無法判斷的問題則切換給真人回應。

目前仍處於演算法開發階段

# 如何啟動這個專案？

1. clone這個專案
2. 參考這篇文章進行設置，並將json檔放入此專案資料夾內與替換掉檔案中的googlesheet連結

[](https://www.maxlist.xyz/2018/09/25/python_googlesheet_crud/)

3. 程式碼中 cc.zh.300.bin 取得(可以直接利用該網址下載）

    ```bash
    # 下載fasttext千錘百鍊預訓練好的詞向量
    !wget https://dl.fbaipublicfiles.com/fasttext/vectors-crawl/cc.zh.300.bin.gz
    !gunzip cc.zh.300.bin.gz
    ```

# 專案內檔案介紹

- Fastext.ipynb
fastext基本功能嘗試
- AutoReply_test
功能開發與測試用
- AutoReply_Final
將測試無誤的function整合
- Generate_data
生成模擬資料
- Corpus.txt
可以自行增加的斷詞語料庫

# 使用技術及參考文章

1. jieba

    [fxsjy/jieba](https://github.com/fxsjy/jieba)

2. database-google drive by pygsheet

    [Worksheet - pygsheets 1.1 documentation](https://pygsheets.readthedocs.io/en/stable/worksheet.html)

3. 決策樹-sklearn 

    [sklearn.tree.DecisionTreeClassifier - scikit-learn 0.24.1 documentation](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)

4. 資料處理-pandas

    [10 minutes to pandas - pandas 1.2.3 documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)

5. 語意處理-fastext

    [Get started · fastText](https://fasttext.cc/docs/en/support.html)

# Future Work

- [ ]  嘗試其他中文語意庫（nltk、CKIP、...等）
- [ ]  決定判斷演算法(決策樹、關鍵字取交集、...嘗試中）
- [ ]  生成模擬資料進行訓練與測試
- [ ]  部署至linebot上