# Group Homework Project

針對高雄市消防局的緊急救護服務統計資料進行分析與報告生成，並利用 C# 撰寫相關程式。


## 資料集來源
本專案使用的資料集來自高雄市消防局的緊急救護服務統計資料，檔名為 `110年高雄市消防局緊急救護服務統計表.xml`。該資料集提供了高雄市每月的救護車服務使用情況，包括送醫次數、未送醫次數、救護車種類等詳細資料。

## 主要程式功能
1. **讀取資料**：
   - 程式會從 `Data` 資料夾中讀取 `110年高雄市消防局緊急救護服務統計表.xml` 檔案，並解析 XML 資料，轉換成 `RescueData` 物件。
   
2. **資料篩選與統計**：
   - 程式會進行基本的資料篩選，如篩選出送醫次數大於 10000 的資料。
   - 計算送醫次數的平均值、最大值、最小值等統計資訊。

3. **輸出至 HTML 檔案**：
   - 根據分析結果，程式會將資料與統計資訊生成 HTML 報告，並儲存至 `HTML` 資料夾中。報告中會顯示表格和統計圖表，幫助更直觀地呈現資料。

4. **圖表顯示**：
   - 使用 `Chart.js` 來生成送醫次數的條形圖，並嵌入至 HTML 報告中。

## 使用的 C# 套件
- **System.Xml.Linq**：用來解析 XML 檔案。
- **System.IO**：用來處理檔案和目錄操作。
- **LINQ**：用來進行資料篩選、排序和統計計算。
- **Chart.js (via CDN)**：用來在 HTML 中顯示統計圖表。

## 如何執行程式
1. 確保您已經安裝 .NET SDK，並且已經有合適的開發環境（例如 Visual Studio 或 Visual Studio Code）。
2. 下載並解壓縮專案檔案，並將 `110年高雄市消防局緊急救護服務統計表.xml` 放置於專案目錄中的 `Data` 資料夾。
3. 開啟專案並編譯執行，程式會讀取資料並生成 HTML 報告。報告會被儲存於專案根目錄下的 `HTML` 資料夾中。
4. 打開 `HTML` 資料夾，並開啟 `RescueDataReport.html` 來查看結果。

## 程式執行結果
執行後，程式會讀取資料、進行統計分析，並將結果以 HTML 格式輸出。報告中包含了每月送醫次數的統計資訊，並以條形圖形式展示送醫次數。您可以在報告中查看每月送醫次數的變化，並了解統計數據如最大、最小和平均送醫次數。

![png](https://github.com/kerong2002/Nkust-113-2/blob/master/HomeWork/OpenData%E5%88%86%E6%9E%90%E8%B3%87%E6%96%99%E7%B7%B4%E7%BF%92/C110152338/ConsoleApp1/ConsoleApp1/PNG/2025-03-28%20112909.png)
![png](https://github.com/kerong2002/Nkust-113-2/blob/master/HomeWork/OpenData%E5%88%86%E6%9E%90%E8%B3%87%E6%96%99%E7%B7%B4%E7%BF%92/C110152338/ConsoleApp1/ConsoleApp1/PNG/2025-03-28%20112943.png)