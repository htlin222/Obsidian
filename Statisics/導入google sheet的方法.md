# 讀取Google sheet
```
library(googlesheets4) #截入googlesheets4 plugin
gs4_deauth() #告訴套件你的google sheet不需要驗證
sheetURL <- "?????" #你的google sheet連結
data_raw <- read_sheet(sheetURL, sheet = "你的表單名稱")
myDataFrame <- as.data.frame(data_raw)
```

# 讀取Excel

## 先安裝跟讀取

  
```
install.packages("openxlsx")

library(openxlsx)
```
  

## 讀取檔案

  
```
# 讀取 Excel 檔案的「工作表1」

df <- read_excel("file.xls", sheet = "工作表1")

  

# 讀取 Excel 檔案的第 1 張工作表

df <- read_excel("file.xls", sheet = 1)
```