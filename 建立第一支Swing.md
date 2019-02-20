<h2>套件</h2>
import javax.swing.*;//JFrame類別定義於javax.swing內<br/>
import java.awt.*;//開發視窗常運用java.awt套件提供的類別
<h2>建立視窗框架</h2>
JFrame frame=new JFrame("視窗名稱");
<h2>取得放置元件的面板</h2>
Container cp=frame.getContentPane();
<h2>宣告按鈕元件</h2>
JButton btn=new JButton("按鈕名稱");
<h2>將元件加入面板</h2>
cp.add(btn);
<h2>設定式窗關閉動作並且調整視窗大小及顯示視窗</h2>
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);//設定按下右上角關閉後將視窗關閉<br/>
frame.pack();//調整視窗大小，否則只會顯示視窗標題列<br/>
frame.setVisible(true);//視窗是否顯示
