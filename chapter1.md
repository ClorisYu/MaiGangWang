### **添加到购物车**

### URL

> /user/shopping

### Example

> PUT /user/shopping?userId=7&token=E12E685B9A222234764C3691082F2B13&goodsId=834&quantity=2&shipWay=2

### Request properties

| **Propertity** | **Description** | **type** |
| :---: | :---: | :---: |
| userId | 用户ID | long |
| token | 用户签名 | str |
| goodsId | 商品ID | Long |
| quantity | 数量 | int |
| shipWay | 出货方式，1-保税仓，2-门店自提 | int |

### Response example

```
{
  "result": 0,
  "msg": "OK",
  "addFlag": 0,
  "total": 8
}
```

### Response properties

| **Propertity** | **Description** | **type** |
| :---: | :--- | :---: |
| result/msg | 请求结果说明，0/OK-成功，1/error-失败，2/Parameter error-参数错误，-1/Token error-token验证失败 | int/str |
| addFlag | 加入状态描述，0-成功，1-超过保税仓单品数量限制（6件，在管理员系统设置），2-超过库存 | int |
| total | 购物车商品总数 | int |



