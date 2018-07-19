# AJK　草刈り機のROSパッケージ  

## 必要環境  
ROS kineticのインストール
  


## 必要な機器  
icart  
北陽のLiDAR  
  


## インストール  
ROSのワークスペースにこのパッケージをダウンロードする。  
  


## 使用方法  
### マッピング  
下記のコマンドを実行する。  
roslaunch icart_hokuyo gmapping.launch  
  
次に下記のコマンドを実行し、ターミナル上からicartを操縦できるようにする。  
rosrun icart_hokuyo key.py  
  
立ち上がったターミナル上でw,a,s,dキー押すことで、icartを操縦できる。  
rvizで確認しながらマッピングを行う。  
  


### 自律走行  
下記のコマンドを実行する。  
roslaunch icart_hokuyo navigation.launch  
  
rvizが立ち上がるので  
"2D Nav Goal"というボタンを押し、地図上をクリック&ドラッグすれば、
任意の場所へ自律走行させることが出来るはずである。