# 前端测试题

## 1.按时间归纳数据

给定一个数组，数组中的元素包含一个创建时间，请按照创建时间的年、月进行整理数据

### 示例

将如下数据

```javascript
[
  { id: 1, created: '2019-11-11 15:12:40', value: '1' },
  { id: 2, created: '2019-11-12 15:12:40', value: '2' },
  { id: 3, created: '2019-12-11 15:12:40', value: '3' },
  { id: 4, created: '2019-12-18 15:12:40', value: '4' },
  { id: 5, created: '2019-12-22 15:12:40', value: '5' },
  { id: 6, created: '2020-01-11 15:12:40', value: '6' }
]

```

转换为：

``` javascript

[{
  year: '2019',
  months: [
    {
      month: '11',
      data: [
        { id: 1, created: '2019-11-11 15:12:40', value: '1' },
        { id: 2, created: '2019-11-12 15:12:40', value: '2' }
      ]
    },
    {
      month: '12',
      data: [
        { id: 3, created: '2019-12-11 15:12:40', value: '3' },
        { id: 4, created: '2019-12-18 15:12:40', value: '4' },
        { id: 5, created: '2019-12-22 15:12:40', value: '5' }
      ]
    }
  ]
},
{
  year: '2020',
  months: [
    {
      month: '01',
      data: [
        { id: 6, created: '2020-11-11 15:12:40', value: '6' }
      ]
    },

  ]
}]
```
