# Badge 徽标

### 介绍

出现在图标或文字右上角的红色圆点、数字或者文字，表示有新内容或者待处理的信息。

### 安装使用

```tsx
import { Badge } from '@quarkd/quark-react'
```

### 徽标独立使用

设置 `content` 属性后，Badge 显示对应的内容，也可以通过设置 `type` 属性为 dot 来显示小红点。

```html
<Badge type="dot"></Badge>
<Badge type="round" content="9"></Badge>
<Badge type="label" content="文字徽标"></Badge>
```

### 徽标类型
徽标支持`dot`、`round`、`label`三种类型，默认为 `round`。

```html
<Badge type="dot">
  <div></div>
</Badge>
<Badge type="round" content="9">
  <div></div>
</Badge>
```

### 徽标大小
徽标大小支持 `normal`、`big` 两种，默认为 `normal`。

```html
<Badge type="dot">
  <div></div>
</Badge>
<Badge content="9">
  <div></div>
</Badge>
<Badge type="dot" size="big">
  <div></div>
</Badge>
<Badge size="big" content="9">
  <div></div>
</Badge>
```

### 徽标风格
徽标边框支持白色边框

```html
<Badge type="label" content="普通徽标">
  <div></div>
</Badge>
<Badge type="label" content="边框徽标" border>
  <div></div>
</Badge>
```
### 数字徽标
数字徽标支持最大值, 超出显示..., 默认最大99

```html
<Badge content="普通徽标">
  <div></div>
</Badge>
<Badge content="100" max="99">
  <div></div>
</Badge>
```
### 自定义样式-背景色

```html
<Badge className="bg-color">
  <div></div>
</Badge>
```
```css
.bg-color {
  --badge-background: linear-gradient(90deg, blue, pink);
}
```



## API
### Props

| 参数         | 说明                               | 类型   | 默认值           |
|--------------|----------------------------------|--------|-----------------|
| type         | 类型，可选值为 `dot` `round` `label` |`string` |`round`         |
| content      | 显示内容                            |`string` |-              |
| size         | 徽标大小，可选值为 `normal` `big`     |`string` |`normal`        |
| border       | 是否显示边框(默认白色)                |`boolean`| `false`        |
| max          | 数字显示最大值                       |`number` | `99`            |

## 样式变量

组件提供了以下[CSS变量](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Using_CSS_custom_properties)，可用于自定义样式，使用方法请参考[主题定制](#/zh-CN/guide/theme)。

| 名称                    | 说明                | 默认值          | 
| -----------------------| --------------------| ---------------|
| `--badge-text-color`     | badge 文字颜色        | `#FFFFFF`        |      
| `--badge-background`     | badge 背景           | `#F72626`        |     
| `--badge-padding-column` | badge 竖直方向内边距   | `2px`            |     
| `--badge-padding-row`    | badge 水平方向内边距   | `4px`           |     
| `--badge-font-size`      | badge 文字大小        | `10px`         |     
| `--badge-font-weight`    | badge 文字粗细        | `500`            |     
| `--badge-dot-size`       | badge dot模式大小     | `6px`            |     
| `--badge-font-family`    | badge font-family    | `跟随系统`        |      
| `--badge-border-color`   | badge 边框颜色        | `#FFFFFF`        |     
