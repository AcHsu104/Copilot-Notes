### 以下案例工具使用

```
AI tool: Copilot
IDE tool: Visual Studio
Plugin: Github Copilot, Github Copilot Chat
```
![截圖 2024-12-24 上午9.51.16](https://hackmd.io/_uploads/ByIC7qwSkg.png)


---


### 1. 用ai協助產生檔案 function 註解描述
- 案例: 提升後續維護 - 新執行/舊有需求, 透過產生註解描述來提升程式碼可讀性, 以利後續維護
- 好處: 減少花費時效 - 協作同仁可以花較少時間看程式碼就能了解其用途, 依照註解描述來暸解其功能, 依註解詳細度約減少10~20%的時間(依程式碼複雜度而定)
- 壞處: 維護性 - 程式異動時, 註解描述未更新, 會造成後續維護人員誤解, 造成程式碼錯誤

    - 透過 IDE 選單觸發 Copilot Plugin
        ![截圖 2024-12-23 下午5.53.25](https://hackmd.io/_uploads/S1eIW9wr1e.png)
    1. 對個別的method or class 協助產生 java doc
    - prompt: /doc 產生想對應產生的 doc 
    ![截圖 2024-12-23 下午4.34.42](https://hackmd.io/_uploads/H1gIb5PB1x.png)
    2. 對所有的method or class 協助產生 java doc
    - 透過Copilot Chat產生所有doc
    ![截圖 2024-12-23 下午4.35.13](https://hackmd.io/_uploads/HJeUW5vrke.png)

    <br>

- 效益: 如有複雜邏輯時, 不需要細看程式碼才知道主要商模運行, 也可以在doc先訂好邊界值(同api doc), 讓後續維護者知道相關邏輯, 依照描述細節省下trace code花費的時間, 初估省下10%時間效益
    
    
<br>
    
### 2. 用ai協助產生測試案例
- 案例: 維持程式品質及提升效率 - 重構/新做程式爲提升程式品質，需要對程式碼進行測試，但測試案例繁多，人為需要花費大量時間進行測試來維護程式品質
- 好處: 提升效率及品質 - 透過ai協助產生測試案例，可以減少人為錯誤，提高測試案例的覆蓋率及品質, 約減少20~30%的時間(依程式碼複雜度而定)
- 壞處: 精確度 - 產生的測試案例可能不夠完整，不夠精確，需要人為進行調整及確認
 
    - 使用IDE Copilot 聊天功能
    ![截圖 2024-12-24 上午10.05.45](https://hackmd.io/_uploads/BJ2-w5PS1l.png)
    
    - ### 產生案例時最好有上下文參照提供範例test(風格較一致)
    1. 對單一檔案function產生案例
    - prompt: /tests 產生邊界值的測試案例
![截圖 2024-12-24 上午10.03.16](https://hackmd.io/_uploads/H1i1v9wrke.png)

    2. 單一檔案產生3A及邊界值案例
    - prompt: /tests 用3A格式產生測試案例, 並要驗證邊界值及描述實作方式
![截圖 2024-12-24 上午10.31.55](https://hackmd.io/_uploads/Sy8wT5wS1e.png)

    - 效益: 透過自動建立測試案例, 讓執行建立單元測試案例能減少花費時間, 並能協助產生一般無考慮到的邊界值案例, 依照複雜度及難易度, 初估約可省下20%時間效益


