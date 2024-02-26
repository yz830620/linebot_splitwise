# linebot_splitwise

### 功能需求
1. 儲存不同line帳號（角色）的消費金額與品項（類別？）
2. 有一個持久化的儲存
3. 有一個後端開放api 給 linebot agent query

#### 後端
* get/ post / update / delete 
    * payment
        * id
        * datetime
        * item name
        * price
    * trip
        * id
        * payments
* audit log
    * operation history
    * state recover
* recover
* report

#### 前端
* awating state
    * [POST] escape trip (NotInTripError)
    * [POST] new payment (NotInTripError)
    * [GET] list trip
    * [POST] new trip
    * [POST] pick trip

* trip state
    * [GET] list payments
    * [DELETE] delete payment
    * [POST] new payment
    * [POST] escape trip
    * [POST] new trip (NotAwatingError)
    * [POST] settle trip
