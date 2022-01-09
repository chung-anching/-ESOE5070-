# 專案執行說明文件
#### *110-1資料庫系統 (ESOE5070) b06501069 鍾安慶*
#### 報告影片連結: https://youtu.be/saVtAMUAvgA

api主要分成三塊: Order、Product、Order
利用express架構建立app這個express 的實例，再利用sqlite3 連接到資料庫 'ESOE5070_final.db'。
- app.get('/user/create') 連到創建電商系統使用者的表單介面user.ejs
- app.get('/products/create') 連到創建電商系統商品的表單介面product.ejs
- app.get('/user') 得到資料庫SELECT過後所有的使用者資料
- app.get('/products') 得到資料庫SELECT過後所有的商品資料
- app.post("/users") 取得表單的request body，在資料庫中創建新使用者
- app.post("/products") 取得表單的request body，在資料庫中創建新商品
- app.get("/user/edit/:id) 取得網址中request的params，將對應到此id的使用者資訊傳到edit.ejs的前端介面
- app.patch("/user/:id") 取得使用者在表單中更新的使用者資料request body ，更新使用者資訊到資料庫
- app.get("/products/:id") 取得網址中request的params，將對應到此id的商品資訊傳到product_edit.ejs的前端介面
- app.patch("/products/:id") 取得使用者在表單中更新的商品資料request body，更新商品資訊到資料庫
- app.get("/products/delete/:id") 取得網址中request的params，將對應到此id的商品資訊傳到"delete.ejs"的前端介面
- app.delete("/products/:id") 將對應到此id的商品從資料庫中刪除
- app.get("/users/signIn") 導到使用者登入login.ejs的前端介面
- app.post("/users/me") 確認信箱、密碼正確之後，導到使用者登入成功後secret.ejs的前端介面
- app.get("/orders/create") 連到創建訂單的表單介面orders.ejs，並帶入使用者的ID
- app.post("/orders") 取得表單orders.ejs的request body，在資料庫中創建新訂單
- app.get('/orders') 得到資料庫SELECT過後所有的訂單資料
- app.get('/orders/:id') 取得網址中request的params，取得對應到此id的訂單資訊

