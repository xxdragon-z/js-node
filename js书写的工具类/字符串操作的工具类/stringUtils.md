# 字符串操作工具类
* ## 更换指定位数的字符串内容
```
export function subFormat(start, end, str, reStr = '*') {
    str = str.toString()
    str = str.split('')
    let newStr = ''
    str.forEach((item, index) => {
        if (index >= start && index <= end)
            newStr += reStr;
        else newStr += item
    })
    return newStr
}
```
* ## 转换金额
``` 
export function formatMoney(str) {
    str = str.toString()
    let newStr = str.split('.')
    if (newStr.length < 2)
        str += '.00'
    else if (newStr[1].length > 2)
        str = str.substring(0, str.indexOf(".") + 2)
    else
        !newStr[1][1] ? str += '0' : ''
    return str;
}
```
