[English Version](README_en.md)
# 智慧型二維線性運動平台(Intelligent Two-Dimensional Linear Motion CNC Plotter)

本專案將介紹有關智慧型二維線性運動平台的設計、製作與應用，屬於**國立臺灣海洋大學 大學生暑期學習實務體驗計畫**。  
- **研究單位**: 國立臺灣海洋大學 電機工程學系  
- **指導教授**: 鄭智湧  
- **成員**: 林昕瑋、陳柔吟

---

## 簡介
本專案旨在設計與製作一台智慧型CNC繪圖平台，利用Arduino開發版控制步進馬達與螺桿，實現高精度的二維運動控制。平台具備自動繪圖與畫風轉換功能，透過電腦傳輸G-code進行繪圖控制與螺桿移動。

---
## 專案特色 
- 高精度二維運動控制
- 支援G-code指令輸入
- 圖片畫風轉換
- 可切換多種繪圖筆

---
## 使用材料 
| 材料          | 規格/型號          |
|---------------|-------------------|
| 開發板        | Arduino UNO       |
| 步進馬達      | 42型 1.7A X 2      |
| 伺服馬達      | SG90               |
| 馬達驅動      | A4988 X 2          |
| 機構          | 鋁型材、金屬螺桿    |
| 電源          | 17V DC             |

---
## 研究方法  
硬體部分採用 V-slot 滑軌與螺桿傳動龍門架，結合 Arduino Uno 與 A4988 + 步進馬達 控制 X-Y 軸，伺服
馬達實現筆尖升降，並以 3D 列印製作支撐架與筆架。軟體以 Python 撰寫，整合 OpenCV 進行圖像處理、
rembg 進行背景移除、Potrace 生成向量路徑，以及 Gemini API 進行風格轉換。系統支援多種繪圖模
式，並能優化路徑後輸出 G-code，透過自製 GUI 完成預覽、匯出與機台控制。

---
## 成果展示  
[示範影片](https://youtu.be/Qn8gQQk7WbQ) 
：
https://youtube.com/playlist?list=PLaIR_ZBq24bLc04j9EN7dDOz_OjDmvVbR&si=acX-4c2rYGbPTH4s

[成果照片資料夾](https://github.com/Aynslielin/CNC-Plotter-Machine/tree/main/Result_Images)  
成果照片:  
![](https://github.com/Aynslielin/CNC-Plotter-Machine/blob/main/Result_Images/PhotoCap_Ghibli_ShapeDraw.jpg)
![](https://github.com/Aynslielin/CNC-Plotter-Machine/blob/main/Result_Images/SelFile_Ghibli_ShapeDraw.jpg)
![](https://github.com/Aynslielin/CNC-Plotter-Machine/blob/main/Result_Images/SelFile_ShapeDraw.jpg)
![](https://github.com/Aynslielin/CNC-Plotter-Machine/blob/main/Result_Images/SelFile_Fill.jpg)
![](https://github.com/Aynslielin/CNC-Plotter-Machine/blob/main/Result_Images/SelFile_Layer.jpg)
![](https://github.com/Aynslielin/CNC-Plotter-Machine/blob/main/Result_Images/SelFile_Potrace.jpg)
![](https://github.com/Aynslielin/CNC-Plotter-Machine/blob/main/Result_Images/SelFile_Sketch.jpg)

---
## 參考文獻  
1.	Arduino. 2025. Download and install Arduino IDE [Internet]. [cited 2025 Sep 2]. Available from: https://support.arduino.cc/hc/en-us/articles/360019833020-Download-and-install-Arduino-IDE

2.	Bolt Taiwan. 2023. 機械螺桿規格表 (Thread data chart) [Internet]. [cited 2025 Sep 2]. Available from: https://bolt-tw.com/technical-information/thread-data-chart/machine-screw/

3.	Chen Fuguo. 2017. A4988步進電機驅動模組使用教學 [Internet]. [cited 2025 Sep 2]. Available from: https://chenfuguo.gitbooks.io/arduino/content/Shields/a4988Controller.html

4.	Cheung Xiongwei. 2024. GRBL的源碼解析 [Internet]. CSDN. [cited 2025 Sep 2]. Available from: https://blog.csdn.net/cheungxiongwei/article/details/135983786

5.	Chris Lee. 2024. 如何使用 Gemini API [Internet]. Medium. [cited 2025 Sep 2]. Available from: https://chrislee0728.medium.com/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8-gemini-api-4458fecbd50f

6.	Data Science Collective. 2025. Turning real photos into Ghibli-style art with Google’s Gemini API for free [Internet]. Medium. [cited 2025 Sep 2]. Available from: https://medium.com/data-science-collective/turning-real-photos-into-ghibli-style-art-with-googles-gemini-api-for-free-e5ddf5949d0e

7.	Digi-Key Forum. 2022. Stepper motor and lead screw discussion [Internet]. [cited 2025 Sep 2]. Available from: https://forum.digikey.com/t/topic/22819

8.	DIY 3D Print. 2013. Adjusting current limit on A4988 stepper driver [Internet]. [cited 2025 Sep 2]. Available from: https://diy3dprint.blogspot.com/2013/11/4988.html

9.	Gnea. 2024. Grbl v1.1 commands [Internet]. GitHub. [cited 2025 Sep 2]. Available from: https://github.com/gnea/grbl/wiki/Grbl-v1.1-Commands

10.	Gnea. 2018. Compiling Grbl via the Arduino IDE [Internet]. GitHub. [cited 2025 Sep 2]. Available from: https://github.com/gnea/grbl/wiki/Compiling-Grbl#via-the-arduino-ide-all-platforms-recommended-for-all-users

11.	Google AI. 2025. Gemini API Quickstart (Python) [Internet]. [cited 2025 Sep 2]. Available from: https://ai.google.dev/gemini-api/docs/quickstart?lang=python&hl=zh-tw

12.	Google AI Studio. 2025. Gemini API Key 管理 [Internet]. [cited 2025 Sep 2]. Available from: https://aistudio.google.com/apikey

13.	Instructables. 2020. GRBL losing steps: 5 simple tips to fix it fast [Internet]. [cited 2025 Sep 2]. Available from: https://www.instructables.com/GRBL-Losing-Steps-5-Simple-Tips-to-Fix-It-Fast--1/

14.	Manuals+. 2021. GRBL CNC Arduino Uno manual (wiring guide) [Internet]. [cited 2025 Sep 2]. Available from: https://manuals.plus/cndy-shield/grbl-cnc-arduino-uno-manual

15.	OctoPrint. 2025. OctoPrint: Open source 3D printer controller [Internet]. GitHub. [cited 2025 Sep 2]. Available from: https://github.com/OctoPrint/OctoPrint

16.	Pololu Forum. 2017. CNC shield and A4988 stepper driver discussion [Internet]. [cited 2025 Sep 2]. Available from: https://forum.pololu.com/t/cnc-shield-and-a-4988-stepper-driver/12686

17.	Pololu Forum. 2011. A4988 heating problem discussion [Internet]. [cited 2025 Sep 2]. Available from: https://forum.pololu.com/t/a4988-stepper-motor-driver-carrier-heating-problem/3474

18.	Potrace. 2019. Potrace: Transforming bitmaps into vector graphics [Internet]. [cited 2025 Sep 2]. Available from: https://potrace.sourceforge.net/

19.	Robottini. 2015. GRBL-servo [Internet]. GitHub. [cited 2025 Sep 2]. Available from: https://github.com/robottini/grbl-servo

20.	Taichi Maker. 2017. Arduino驅動A4988步進電機教學 [Internet]. [cited 2025 Sep 2]. Available from: http://www.taichi-maker.com/homepage/reference-index/motor-reference-index/arduino-a4988-nema-stepper-motor/

21.	Thingiverse. 2017. Drawing Robot project [Internet]. [cited 2025 Sep 2]. Available from: https://www.thingiverse.com/thing:2349232

22.	維度科技. 2025. Klipper 與 Marlin 差異比較 [Internet]. [cited 2025 Sep 2]. Available from: https://diman.tw/news-Detail/klipper-vs-marlin-difference

23.	Arduino Forum. 2023. Drivers on CNC shield heating up fast [Internet]. [cited 2025 Sep 2]. Available from: https://forum.arduino.cc/t/drivers-on-cnc-shield-heating-up-fast/1182255/4

24.	Arduino Forum. 2022. Overheating stepper motor controllers [Internet]. [cited 2025 Sep 2]. Available from: https://forum.arduino.cc/t/overheating-stepper-motor-controllers/963394

25.	A4988的工作原理，引腳和功能 [Internet]. [Cited 2025 Sep 8]. Available from: https://www.ariat-tech.tw/blog/a4988-working-principle,pinout-and-features.html

---
