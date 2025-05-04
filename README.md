# ディスプレイ表示用 画像コード作成用Excelの公開
## １　前提
Arduino UNOにディスプレイACROBOTIC SSD1306を接続
なんか未開発なところがあるっぽいので下記参考にして.cppと.hファイルを修正する

http://www.takishita.jp/toy_hospital/staff_blog/ch32v003-oled-ssd1306-library
  
修正しないとHelloサンプルすらコンパイルエラーした
  
## ２　画像表示について
ベースはgitでゲット。これ自体はロボットイラストが表示されるサンプルですが記載方法の参考に。
  
https://github.com/datasith/Ai_Ardulib_SSD1306/tree/main/examples/DrawLogo

8x8ドットで１文字、１行16文字、８行表示、トップ２行は黄色、３行目から８行目は水色で表示されます
  
![スクリーンショット 2025-05-04 173506](https://github.com/user-attachments/assets/d02e15ed-cd8f-4dd3-a839-19930fc84290)

（色が自由だったらすません、未確認です

ドットの点灯はこんな感じでビットで判断してます
  
![qiita01](https://github.com/user-attachments/assets/c7a0590c-b82c-4020-84dd-1e1da222690e)


ここまでわかれば一応何でも表示できますね！！気合いと根性があれば…
  
## ３　何でもいいのでイラストを描きます
４にスキップしてもいいですが、画像エディタで試作しておくと描くのは楽かもということで一度画像を起こします

![TEST](https://github.com/user-attachments/assets/422a0a1c-061c-4ef2-8f75-71f683f3423c)

## ４　Excelにドットを転記してコードを成型
Excelに気合いでドット打って１を埋めていきます。同時にシート上部の黄色個所に成形されたコードが表示されます

１６進に変換します。ここツールあれば楽なんですがちょっと無さそうなのでExcelで自作しました。

[sample.xlsx](https://github.com/user-attachments/files/20026852/sample.xlsx)
![スクリーンショット 2025-05-04 182856](https://github.com/user-attachments/assets/acc29776-1994-4e76-bda8-8d07caea9180)

成形されたらテキストエディタでTab文字を除去してArduinoのコードに貼り付けてみましょう。
  
<img width=400 src="https://github.com/user-attachments/assets/bc6ce12a-7248-40e1-93bd-4e32c7fe36d1">

やったぜ！
  
