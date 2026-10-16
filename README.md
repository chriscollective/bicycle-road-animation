# 單車騎乘路線動畫（bicycle-road-animation）

輸入起點與終點，在開源地圖上以動畫畫出自行車騎乘路線，並估算距離、騎乘時間與各段抵達時刻。預設路線為「淡水捷運站 → 白沙灣 → 淡水捷運站」。

**線上展示：<https://chriscollective.github.io/bicycle-road-animation/>**

## 功能

- 地圖底圖：[CyclOSM](https://www.cyclosm.org)（自行車專用圖磚）與 [OpenStreetMap](https://www.openstreetmap.org) 標準圖，可切換
- 路線計算：[OSRM](https://routing.openstreetmap.de) 自行車模式，依 OpenStreetMap 真實道路資料
- 地點查詢：[Nominatim](https://nominatim.openstreetmap.org)，也可輸入「緯度,經度」或在地圖上點選終點
- 來回 / 單程切換，去程橘色、回程藍色
- 配速選擇與出發時間，自動算出每 5 公里與終點的預計抵達時間
- 路線逐段畫出的動畫：規劃好路線後按「▶ 播放動畫」才開始播放，可重複播放
- 鏡頭跟隨：把地圖放大後再按播放，鏡頭會跟著單車移動；拖曳地圖即可停止跟隨

## 使用方式

本專案是單一 HTML 檔，不需要安裝套件。請透過網頁伺服器開啟（直接雙擊檔案會被 OpenStreetMap 擋下圖磚與查詢）：

```bash
python -m http.server 8765
```

然後在瀏覽器開啟 <http://127.0.0.1:8765/>。

## 注意事項

- 騎乘時間依所選配速估算，未含休息、紅綠燈與坡度影響
- 地圖與路線服務為公開免費服務，請勿大量自動化請求

## 授權與資料來源

地圖資料 © OpenStreetMap 貢獻者，以 ODbL 授權。
