# i-Cart eduをmove_baseで自律走行  

## 必要環境  
ROS kineticのインストール
  


## 必要な機器  
i-Cart edu  
北陽のLiDAR  
  


## インストール  
下記のコマンドによりROSのワークスペースにこのパッケージをダウンロードする。  
cd catkin_ws/src
git clone https://github.com/IgarashiBME/icart_hokuyo  
  
関連パッケージを下記のコマンドでインストールする。  
sudo apt update  
sudo apt install ros-kinetic-slam-gmapping  
sudo apt install ros-kinetic-urg-node  
sudo apt install ros-kinetic-map-server ros-kinetic-move-base  
sudo apt install ros-kinetic-amcl ros-kinetic-dwa-local-planner  
sudo apt install ros-kinetic-navigation  
  


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