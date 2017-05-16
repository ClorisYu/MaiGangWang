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
| result/msg | 0/OK-成功，2/ | int/str |
| addFlag | 加入状态描述，0-成功，1-超过保税仓单品数量限制（6件，在管理员系统设置），2-超过库存 | int |
| total | 购物车总商品数量 | int |
| shoppingCartList | 删除后的购物项列表（按出货方式倒序，先门店自提，后保税仓发货；按加入购物车的时间倒序，后加入的在前面） | 对象数组 |
| id |  |  |
| ... |  |  |



