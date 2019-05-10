# 验证js
* ## 验证数字，可自定义长度
```
export function regexNum(val,min,max) {
    let regexNum =new RegExp('\\d{'+min+(max?','+max+'}':'}'))
        return regexNum.test(val)
}
```