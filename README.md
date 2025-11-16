# aardio 扩展库 time.tyme 
 
万年历与农历组件。  
翻译自 [Tyme](https://github.com/6tail/tyme4ts) ，基本保持原接口与用法不变。  

## 调用范例

```aardio 
import console;
import time.tyme;

var SolarDay = time.tyme.SolarDay;
 
// 使用 time 对象指定的时间创建公历日对象
var solar = SolarDay.fromYmd( time() );

// 也可以传入指定 year, month, day 字段的表对象
solar = SolarDay.fromYmd( year = 1986,month=5,day=29 );

// 指定年月日参数，创建公历日对象
solar = SolarDay.fromYmd(1986, 5, 29);

// 所有 tyme 对象基本都可以用 tostring 转换为字符串
var str = tostring(solar);

// 1986年5月29日
console.log( solar ); // console.log 参数自动调用 tostring 

// 农历丙寅年四月廿一
console.log( solar.getLunarDay() ); 

// 第十七饶迥火虎年四月廿一
console.log( solar.getRabByungDay() ); 

console.pause();
```

## 关于前端版本

在 aardio 中也可以通过 web.view  直接调用 Tyme 或 lunar 前凋版本，我写的教程与例子：

[AI 编程入门：炫酷桌面万年历（农历、透明背景、3D 翻转动画）](https://mp.weixin.qq.com/s/XQLfulXHTm3XaryyowZKrg)

运行效果：

![桌面万年历](./screenshots/lunar.jpeg)

动画：

![桌面万年历-动画效果](./screenshots/lunar.gif)