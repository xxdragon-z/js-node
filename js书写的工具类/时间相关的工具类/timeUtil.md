# time工具类
* ## 根据秒,获取mm:ss 的时间
```
const  formatDateBySecond=s=>{
  let min=formatNumber(Math.floor(s/60))
  let sec=formatNumber(s%60)
  return min+':'+sec
}
```
* ## 时间转化为Y/M/s hh:mm:ss
```
const formatTime = date => {
  const year = date.getFullYear()
  const month = date.getMonth() + 1
  const day = date.getDate()
  const hour = date.getHours()
  const minute = date.getMinutes()
  const second = date.getSeconds()

  return [year, month, day].map(formatNumber).join('/') + ' ' + [hour, minute, second].map(formatNumber).join(':')
}
```
* ## 补全时分秒
```
const formatNumber = n => {
  n = n.toString()
  return n[1] ? n : '0' + n
}
```