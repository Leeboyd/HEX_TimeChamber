The F2E - 前端修練精神時光屋
===
臉書連結：[The F2E - 前端修練精神時光屋](https://www.facebook.com/groups/173311386703334/?ref=group_header)

## 1. [No1.todolist](https://www.facebook.com/groups/173311386703334/permalink/179453469422459/)

> 觀看設計稿：https://bit.ly/2HfaR2M

### 工作日誌

> 2018-06-04

1. create `git` Repository of `HEX1`
2. setting up backend application

> 2018-06-05

1. Create Heroku Application
  a. `heroku create --ssh-git`
  b. `heroku buildpacks:set heroku/nodejs`
  
2. Push changes to Heroku (heroku) master; triggering Heroku to build the staging (doubling as production) application.
  a. `git push heroku master`
  b. `heroku open`

3. Push changes to GitHub (origin) master

4. at `HEX1` repo. add `/backend` to submodule
  *. `git submodule add git@github.com:Leeboyd/HEX_TimeChamber_Backend.git backend`

5. 使用 SaaS 服務 mLab 提供的 Mongo database
  a. 在 heroku Overview 中 add-ons 找到 `mLab MongoDB`，並加入專案（需信用卡）
  b. 在 heroku Resource 中，連到 mLab 網站，這時 heroku 已在 幫我們 new MongoDB
  c. 建立一位 user，輸入帳號密碼

6. 取得 URI
  * 為避免在程式中寫死帳號密碼，我們把帳密加到 heroku 的環境變數
  * `heroku config:set <變數名>=mongodb://<帳號>:<密碼>@<主機位置>:<PORT>/<資料庫名>`
  * 查看 URI `heroku config:get MONGODB_URI`

7. Connecting to MongoDB instance



