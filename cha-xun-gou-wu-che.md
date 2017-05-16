### 查询购物车

### URL

> /user/shopping

### Request example

> GET /user/shopping?userId=9&token=31FED15E20B05584AFA3F6C003CBCE71

### Request properties

| **Property** | **Description** | **type** |
| :--- | :--- | :--- |
| userId | 用户ID | Long |
| token | 用户签名 | str |

### Response example

```
{
  "result": 0,
  "msg": "OK",
  "total": 4,
  "shoppingCartList": [
    {
      "id": 17,
      "userId": 7,
      "goodsId": 834,
      "oldPrice": 120,
      "quantity": 4,
      "shipWay": 2,
      "imgpath": "http://ogv8jirtz.bkt.clouddn.com/Fts05itpIhUXgQ-uCMuLdJ0Vsiry",
      "title": "花王Merries牌|花王三倍透气系列|NB |90枚/包|1.5kg|纸尿裤",
      "price": 120,
      "marketPrice": 158,
      "warestock1": 200,
      "warestock2": 200,
      "warestock3": 0
    }
  ]
}
```

### Response properties

| **Property** | **Description** | **type** |
| :--- | :--- | :--- |
| result/msg | 0/OK-成功，-1/Token error-token错误 | int/str |
| total | 购物车总商品数量 | int |
| shoppingCartList | 购物项列表（按出货方式倒序，先门店自提，后保税仓发货；按加入购物车的时间倒序，后加入的在前面） | 对象数组 |
| id | 购物项ID | Long |
| userId | 用户ID | Long |
| goodsId | 商品ID | Long |
| oldPrice | 上次修改/加入购物车时的商品价格 | BigDecimal |
| quantity | 该商品购买数量 | int |
| shipWay | 出货方式（1-保税仓发货，2-门店自提） | int |
| imgpath | 商品基本图片路径 | str |
| title | 商品标题 | str |
| price | 商品卖价 | BigDecimal |
| marketPrice | 商品参考价（市场价） | BigDecimal |
| warestock1 | 自提库存 | int |
| warestock2 | 保税仓库存 | int |
| warestock3 | 门店库存 | int |



