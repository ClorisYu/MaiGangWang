### 删除购物项

### URL

> /user/shopping

### Request example

> DELETE /user/shopping?userId=7&token=E12E685B9A222234764C3691082F2B13&ids=17,27

删除ID为17和27的两条购物项

### Request properties

| **Property** | **Description** | **Type** |
| :--- | :--- | :--- |
| userId | 用户ID | long |
| token | 签名 | str |
| ids | 购物项ID构成的数组（JSON里用英文逗号连接） | 整型数组 |

### Response example

```
{
  "result": 0,
  "msg": "OK",
  "addFlag": 0,
  "total": 0,
  "shoppingCartList": []
}
```

### Response properties

| **Property** | **Description** | **type** |
| :--- | :--- | :--- |
| result/msg | 0/OK-成功，-1/Token error-token错误 | int/str |
| total | 购物车总商品数量 | int |
| shoppingCartList | 删除后的购物项列表（按出货方式倒序，先门店自提，后保税仓发货；按加入购物车的时间倒序，后加入的在前面） | 对象数组 |
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



