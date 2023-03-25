Pytorch LSTMによる罹患者数予測

コロナウィルス罹患者数推移から  
国内全体の日毎の累積罹患者数を2週間先まで予測するシンプルなPytorch LSTMモデルです。  

【モデル概要】Pytorch LSTM  
・data:signage COVID-19 Case Dataset（罹患者統計）  
・optimizer = Adam  
・criterion = MSE  
  
地域によって推移が異なるため、近隣で似た傾向を持つ9つのグループに都道府県を分ける  
そのグループごとにモデルを作成し、直前14日間がうまく予測できるようにハイパーパラメータとepochを調整
