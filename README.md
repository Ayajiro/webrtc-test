# WebRTC Test

After finish Google Codelabs [Real time communication with WebRTC](https://codelabs.developers.google.com/codelabs/webrtc-web), try to rewrite socket.io with heigher version as practise.

THIS REPO IS NOT FINISH.

[Some WebRTC samples](https://github.com/webrtc/samples?tab=readme-ov-file)

# WebRTC 練習專案 - 工作清單

## 📌 1. 初始化專案
- [ ] 設置前端與後端環境  
  - [ ] 初始化 **Node.js** 後端 (`express + websocket`)  
  - [x] 初始化 **前端** (`React + TailwindCSS`)  
  - [ ] 設定 WebRTC 必要的前端架構 (`RTCPeerConnection`)  

## 📌 2. 建立房間管理
- [ ] 前端 UI：使用者可創建/加入房間  
  - [ ] 設計 UI（輸入房間 ID、新增房間按鈕）  
  - [ ] 房間建立時可選擇是否 **使用密碼**  
  - [ ] 顯示房間內的使用者列表  

- [ ] 後端：管理房間與連線  
  - [ ] 使用 `socket.io` 建立 WebSocket 伺服器  
  - [ ] 處理房間創建與密碼驗證（如果有）  
  - [ ] 處理用戶加入與離開房間的事件  

## 📌 3. WebRTC 訊號交換（Signaling）
- [ ] **WebRTC 連線建立**  
  - [ ] 前端初始化 `RTCPeerConnection`  
  - [ ] 使用 `socket.io` 傳遞 `offer` / `answer` 訊號  
  - [ ] 交換 ICE 候選資訊 (`onicecandidate`)  
  - [ ] 建立點對點視訊/音訊流 (`getUserMedia()`)  

## 📌 4. 音訊控制
- [ ] **開關音訊**
  - [ ] UI 上新增 **靜音 / 解除靜音** 按鈕  
  - [ ] 使用 `track.enabled = false` 來關閉麥克風  
  - [ ] 透過 `socket.io` 廣播音訊狀態變更  

## 📌 5. 切換視訊來源
- [ ] **螢幕分享與攝影機切換**
  - [ ] UI 上新增 **切換視訊來源** 按鈕  
  - [ ] 使用 `getDisplayMedia()` 啟動螢幕分享  
  - [ ] 使用 `replaceTrack()` 切換回攝影機  
  - [ ] 透過 `socket.io` 廣播視訊來源狀態變更  

## 📌 6. 優化與錯誤處理
- [ ] **錯誤處理與體驗優化**
  - [ ] 處理 **連線失敗** 或 **對方離線** 的情境  
  - [ ] 增加 **房間內訊息**（如「XXX 已加入房間」）  
  - [ ] 顯示 **視訊來源狀態**（攝影機 / 螢幕分享）  
  - [ ] 提供 **離開房間** 按鈕  
