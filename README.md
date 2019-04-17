# DateTimewallpaper_Communication

## 自定义配置说明

## 字段解释

### 全局字段

| 字段        |      解释      |
|----------  |:-------------:|
| centerTextSize      |  全局中心文字大小,默认90       |
| circleTextSize      |  全局外圈文字大小,默认50       |
| cusFont      |  全局外置字体文件名 (请将字体文件拷贝到"手机存储/时间轮盘"目录)      |
| centerText |  表盘中心绘制内容 |
| circleText |  表盘四周绘制内容 |

### 局部字段

| 字段        |      解释      |
|----------  |:-------------:|
| type       |  绘制类型       |
| array      |  绘制文字       |
| bold       |  加粗   （0不使用 1使用  默认0 ）   |
| useCusFont      |  使用外置字体（ 0不使用 1使用  默认0   ） |

### type类型

| 字段        |      解释      | array参数示例|
|----------  |:-------------:|:-------------|
| week       |  周            | ["周日","周一","周二","周三","周四","周五","周六"]
| month      |  月            | ["壹","贰","仨","肆","伍","陆","柒","捌","玖","拾","拾壹","拾贰"]
| day        |  日            | [" 壹"," 贰"," 叁"," 肆"," 伍"," 陆"," 柒"," 捌"," 玖"," 拾","拾壹","拾贰","拾叁","拾肆","拾伍","拾陆","拾柒","拾捌","拾玖","贰拾","贰拾壹","贰拾贰","贰拾叁","贰拾肆","贰拾伍","贰拾陆","贰拾柒","贰拾捌","贰拾玖","叁拾","叁拾壹"]
| hour       |  时            |[" 壹"," 贰"," 叁"," 肆"," 伍"," 陆"," 柒"," 捌"," 玖"," 拾","拾壹","拾贰"]
| minute     |  时            |[" 壹"," 贰"," 叁"," 肆"," 伍"," 陆"," 柒"," 捌"," 玖"," 拾","拾壹","拾贰","拾叁","拾肆","拾伍","拾陆","拾柒","拾捌","拾玖","贰拾","贰拾壹","贰拾贰","贰拾叁","贰拾肆","贰拾伍","贰拾陆","贰拾柒","贰拾捌","贰拾玖","叁拾","叁拾壹","叁拾贰","叁拾叁","叁拾肆","叁拾伍","叁拾陆","叁拾柒","叁拾捌","叁拾玖","肆拾","肆拾壹","肆拾贰","肆拾叁","肆拾肆","肆拾伍","肆拾陆","肆拾柒","肆拾捌","肆拾玖","伍拾","伍拾壹","伍拾贰","伍拾叁","伍拾肆","伍拾伍","伍拾陆","伍拾柒","伍拾捌","伍拾玖"," 零"]
| second     |  秒            |[" 壹"," 贰"," 叁"," 肆"," 伍"," 陆"," 柒"," 捌"," 玖"," 拾","拾壹","拾贰","拾叁","拾肆","拾伍","拾陆","拾柒","拾捌","拾玖","贰拾","贰拾壹","贰拾贰","贰拾叁","贰拾肆","贰拾伍","贰拾陆","贰拾柒","贰拾捌","贰拾玖","叁拾","叁拾壹","叁拾贰","叁拾叁","叁拾肆","叁拾伍","叁拾陆","叁拾柒","叁拾捌","叁拾玖","肆拾","肆拾壹","肆拾贰","肆拾叁","肆拾肆","肆拾伍","肆拾陆","肆拾柒","肆拾捌","肆拾玖","伍拾","伍拾壹","伍拾贰","伍拾叁","伍拾肆","伍拾伍","伍拾陆","伍拾柒","伍拾捌","伍拾玖"," 零"]
| text       | 自定义文字      |["我","最","帅"]
| dateformat | 时间格式        | ["YYYY-MM-dd"]
| hour_23_23 | 时辰        | ["子时","丑时","寅时","卯时","辰时","巳时","午时","未时","申时","酉时","戌时","亥时"]

## 示例


**有效配置没有下面的注释，注释只是方便理解**

**更多的示例配置在conf目录**

```json
{
  //中心文字
  "centerTextSize": 90,
  "circleTextSize": 50,
  "cusFont": "xx.ttf", //字体文件名
  "centerText": [
    { 
      "bold": 1,  //加粗
      "useCusFont": 1, //使用自定义字体
      "type": "week", //类型 week 周 month月 day日 hour时 minute分 second秒 text 自定义文字 dateformat 时间格式
      //字符数组
      "array": [ 
        "周日",
        "周一",
        "周二",
        "周三",
        "周四",
        "周五",
        "周六"
      ]
    },
    {
      //时间格式类型
      "type": "dateformat", 
      "array": [
        "yyyy-MM-dd"
      ]
    },
    {
      "type": "ampm",
      "array": [
        "上午",
        "下午"
      ]
    }
  ],
  //四周文字
  "circleText": [
    {
      "type": "month",
      "array": [
        "壹",
        "贰",
        "仨",
        "肆",
        "伍",
        "陆",
        "柒",
        "捌",
        "玖",
        "拾",
        "拾壹",
        "拾贰"
      ]
    },
    {
      "type": "text",
      "array": [
        "月"
      ]
    },
    {
      "type": "day",
      "array": [
        " 壹",
        " 贰",
        " 叁",
        " 肆",
        " 伍",
        " 陆",
        " 柒",
        " 捌",
        " 玖",
        " 拾",
        "拾壹",
        "拾贰",
        "拾叁",
        "拾肆",
        "拾伍",
        "拾陆",
        "拾柒",
        "拾捌",
        "拾玖",
        "贰拾",
        "贰拾壹",
        "贰拾贰",
        "贰拾叁",
        "贰拾肆",
        "贰拾伍",
        "贰拾陆",
        "贰拾柒",
        "贰拾捌",
        "贰拾玖",
        "叁拾",
        "叁拾壹"
      ]
    },
    {
      "type": "text",
      "array": [
        "日"
      ]
    },
    {
      "type": "hour",
      "array": [
        " 壹",
        " 贰",
        " 叁",
        " 肆",
        " 伍",
        " 陆",
        " 柒",
        " 捌",
        " 玖",
        " 拾",
        "拾壹",
        "拾贰"
      ]
    },
    {
      "type": "text",
      "array": [
        "时"
      ]
    },
    {
      "type": "minute",
      "array": [
        " 壹",
        " 贰",
        " 叁",
        " 肆",
        " 伍",
        " 陆",
        " 柒",
        " 捌",
        " 玖",
        " 拾",
        "拾壹",
        "拾贰",
        "拾叁",
        "拾肆",
        "拾伍",
        "拾陆",
        "拾柒",
        "拾捌",
        "拾玖",
        "贰拾",
        "贰拾壹",
        "贰拾贰",
        "贰拾叁",
        "贰拾肆",
        "贰拾伍",
        "贰拾陆",
        "贰拾柒",
        "贰拾捌",
        "贰拾玖",
        "叁拾",
        "叁拾壹",
        "叁拾贰",
        "叁拾叁",
        "叁拾肆",
        "叁拾伍",
        "叁拾陆",
        "叁拾柒",
        "叁拾捌",
        "叁拾玖",
        "肆拾",
        "肆拾壹",
        "肆拾贰",
        "肆拾叁",
        "肆拾肆",
        "肆拾伍",
        "肆拾陆",
        "肆拾柒",
        "肆拾捌",
        "肆拾玖",
        "伍拾",
        "伍拾壹",
        "伍拾贰",
        "伍拾叁",
        "伍拾肆",
        "伍拾伍",
        "伍拾陆",
        "伍拾柒",
        "伍拾捌",
        "伍拾玖",
        " 零"
      ]
    },
    {
      "type": "text",
      "array": [
        "分"
      ]
    },
    {
      "type": "second",
      "array": [
        " 壹",
        " 贰",
        " 叁",
        " 肆",
        " 伍",
        " 陆",
        " 柒",
        " 捌",
        " 玖",
        " 拾",
        "拾壹",
        "拾贰",
        "拾叁",
        "拾肆",
        "拾伍",
        "拾陆",
        "拾柒",
        "拾捌",
        "拾玖",
        "贰拾",
        "贰拾壹",
        "贰拾贰",
        "贰拾叁",
        "贰拾肆",
        "贰拾伍",
        "贰拾陆",
        "贰拾柒",
        "贰拾捌",
        "贰拾玖",
        "叁拾",
        "叁拾壹",
        "叁拾贰",
        "叁拾叁",
        "叁拾肆",
        "叁拾伍",
        "叁拾陆",
        "叁拾柒",
        "叁拾捌",
        "叁拾玖",
        "肆拾",
        "肆拾壹",
        "肆拾贰",
        "肆拾叁",
        "肆拾肆",
        "肆拾伍",
        "肆拾陆",
        "肆拾柒",
        "肆拾捌",
        "肆拾玖",
        "伍拾",
        "伍拾壹",
        "伍拾贰",
        "伍拾叁",
        "伍拾肆",
        "伍拾伍",
        "伍拾陆",
        "伍拾柒",
        "伍拾捌",
        "伍拾玖",
        " 零"
      ]
    },
    {
      "type": "text",
      "array": [
        "秒"
      ]
    }
  ]
}
```
