Devonthink 版

按鍵觸發
跳出通知「你正在選取mode中」
模擬選取後放開
Copy
將系統剪貼簿存入變數content中
if 在edge, safari, chrome中 then
	觸發插件功能
	將網頁址及來源的markdown加入content中
elseif 在Devonthink中
	if 可以複製page link then
		將page link 加入content中
	else
		將item link 加入content中
else
	Do nothing
> 這時你已經有內容了

打開Devonthink
新增分頁
以範例新增一條筆記
貼上內容
存檔