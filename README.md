# 前端测试题

## 1.按时间归纳数据

给定一个数组，数组中的元素包含一个创建时间，请按照创建时间的年、月进行整理数据

**示例：**

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

## 2.按照时间变换颜色

给定一个div和一个数组，数组元素包含一个数字time和一个颜色color。从数组的第一个元素开始遍历，将div背景颜色设置为该元素提供的颜色，然后经过time秒后将div设置为下一个元素的颜色

**示例：**

给定数组

```javascript
[{ time: 1, color: 'red' }, { time: 2, color: 'blue' },{ time: 3, color: 'green'}]

```

div应该变成1秒红色，然后2秒蓝色，然后3秒绿色

## 3.树状结构包含问题

给以下定数据结构,实现方法判断treeNode1是否完全包含treeNode2

```typescript

interface TreeNode {
  val: number
  children?: TreeNode[]
}

```

**完全包含定义:**

所有treeNode2中的节点，都在treeNode1中出现，并且treeNode2中节点的父子关系在treeNode1中保持不变

**示例：**

包含

![avatar](/asset/include.png)

不包含

![avatar](/asset/exclude.png)
