# tokyo_temp
### 気象庁による東京の日平均気温の月平均値のインポート
import pandas as pd

df = pd.read_html("https://www.data.jma.go.jp/obd/stats/etrn/view/monthly_s3.php?prec_no=44&block_no=47662")[0]
df.set_index("年", inplace=True)
display(df)

print(df.info())


