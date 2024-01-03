# 使用matplotlib plt畫圖無法顯示中文
# 下載 NotoSansTC-VariableFont_wght.ttf 中文字型 wget.download("https://github.com/jamesallin/ChineseFont/raw/main/NotoSansTC-VariableFont_wght.ttf")
# 使用 matplotlib 模組的 rc() 函式, 套用字型 mlp.rc('font',family="Noto Sans TC")
!pip install wget
import wget
wget.download("https://github.com/jamesallin/ChineseFont/raw/main/NotoSansTC-VariableFont_wght.ttf")

import matplotlib.pyplot as plt
import matplotlib as mlp
from matplotlib.font_manager import fontManager
fontManager.addfont("NotoSansTC-VariableFont_wght.ttf")
mlp.rc('font',family="Noto Sans TC")
# 設定dataframe
import pandas as pd
data =  {'a': [1,2,3],'b': [10, 20, 30]}
x=data['a']
y=data['b']
# 用plt畫出xy圖
plt.scatter(x,y)
plt.title("數字")
plt.show()
