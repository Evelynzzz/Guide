#### 发起 key value 交易
```go
// 准备参数
reqFunc := "value"
reqMethod := "POST"
params := map[string]interface{}{"key": "2020-02-12", "value": "1111"}
// 进行请求
fmt.Println(KeyValueList(reqFunc, reqMethod, params))
```
```json
{
  'code': 0, 
  'message': 'Success',
}
```

#### 查看 key value 交易
```go
// 准备参数
reqFunc := "value"
reqMethod := "GET"
params := map[string]interface{}{"key": "2020-02-12"}
// 进行请求
fmt.Println(KeyValueList(reqFunc, reqMethod, params))
```
```json
{
    "code": 0,
    "data": {
        "key": "2020-02-12",
        "value": "1111"
    },
    "message": "Success"
}
```

#### 发起 key list 交易
```go
// 准备参数
reqFunc := "list"
reqMethod := "POST"
params := map[string]interface{}{"key": "2020-02-12_list", "value": "1111"}
// 进行请求
fmt.Println(KeyValueList(reqFunc, reqMethod, params))
```
```json
{
  'code': 0, 
  'message': 'Success',
}
```

#### 查看 key list 交易
```go
// 准备参数
reqFunc := "list"
reqMethod := "GET"
params := map[string]interface{}{"key": "2020-02-12_list"}
// 进行请求
fmt.Println(KeyValueList(reqFunc, reqMethod, params))
```
```json
{
    "code": 0,
    "data": {
        "key": "2020-02-12_list",
        "list": [
            "1111"
        ]
    },
    "message": "Success"
}
```

#### 查看当前块高
```go
fmt.Println(BlockCount())
```
```json
{
    "code": 0,
    "count": 322,
    "message": "Success"
}
```

#### 查看交易总数
```go
fmt.Println(TransactionCount())
```
```json
{
    "code": 0,
    "count": 912,
    "message": "Success"
}
```

#### 查看当前节点数
```go
fmt.Println(NodeCount())
```
```json
{
    "code": 0,
    "count": 3,
    "message": "Success"
}
```

#### 查看当前存储空间大小，单位为bytes
```go
fmt.Println(DataSize())
```
```json
{
    "code": 0,
    "size": 4435219.0,
    "message": "success"
}
```