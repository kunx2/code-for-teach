程式檔案內有部分註解，若有不清楚的部分再問


image_capture用於建立資料庫   用對比的方式擷取出物件，可以用素色的布或牆壁當作背景


取出來的28x28彩色圖片 資料處理(ex:灰階、二值化、降維、tag)後可以丟入你們之前的神經網路進行訓練


dataset_tag 直接將圖片檔名更改當作tag


classifier用於訓練及實際測試


裡面有些跟檔案路徑有關的部分需自行更改


---------------------------------------------------------------------------------------------


操作說明：


1.先將一種物品放在拍攝區，用image_capture抓取影像，若是無法抓到可以將內部的canny參數調低
![註解 2020-10-23 185029](https://user-images.githubusercontent.com/72076184/96995363-a9845d80-1560-11eb-82f0-1b11d018cf51.png)

2.用dataset_tag將其標註，再將tag的sort加1，並刪除標記前的資料(有多種類別的物品就重複拍攝並標記)
![註解 2020-10-23 185421](https://user-images.githubusercontent.com/72076184/96995708-30d1d100-1561-11eb-8f0a-0a28dea800fb.png)

(也可以用手動標記及擷取)


3.用training的程式訓練並測試(內部的網路架構及參數(學習率、bias等)可自行調整)

同樣的若抓不到就將canny參數調低
