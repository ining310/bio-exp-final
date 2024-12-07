# bio-exp-final
113-1  電工實驗(生醫工程) 期末專題

demo 影片： https://youtu.be/0K_HwAe107s
說明：
以 v8 檔案為例，python 模擬每次讀取一分鐘之 EEG、ECG signal，回傳 asleepTime (AT) "00:15" (第15分鐘睡著) 給 Arduino，Arduino 計算睡眠時長(SD)+睡著時間(AT)=鬧鈴時間(BT)，利用 DS3231 時間模組判斷時間，當 BT 到達時 蜂鳴器響起。

影片中上床（開始測量）時間為 "02:50"，APP 設定的睡覺時常(SD) 為 "00:10"。開始測量後 python 每分鐘（以 1 秒模擬實際上 1 分鐘）會傳該分鐘 HR、整個 SDNN 與健康風險（經過Arduino）送到 APP，並作圖睡眠時間之 HR 趨勢。由於 EEG model 在第 15 分鐘偵測到 Spindle，回傳給 Arduino，計算 BT，並在 BT+SD = 15 分鐘（影片中的 15 秒）蜂鳴器響起。
