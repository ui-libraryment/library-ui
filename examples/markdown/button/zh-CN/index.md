
# Button 按钮

常用的操作按钮。

### 基础用法

:::demo

```html
<div class="row flex-row">
  <as-button>默认按钮</as-button>
  <as-button style="margin-left:20px" type="info">信息按钮</as-button>
  <as-button style="margin-left:20px" type="primary">原始按钮</as-button>
  <as-button style="margin-left:20px" type="success">成功按钮</as-button>
  <as-button style="margin-left:20px" type="error">错误按钮</as-button>
  <as-button style="margin-left:20px" type="warning">警告按钮</as-button>
</div>
```

:::

### 纯色(plain) button

:::demo

```html
<div class="flex-row" style="margin-top: 10px">
  <as-button plain>默认按钮</as-button>
  <as-button style="margin-left:20px" type="info" plain>信息按钮</as-button>
  <as-button style="margin-left:20px" type="primary" plain>原始按钮</as-button>
  <as-button style="margin-left:20px" type="success" plain>成功按钮</as-button>
  <as-button style="margin-left:20px" type="error" plain>错误按钮</as-button>
  <as-button style="margin-left:20px" type="warning" plain>警告按钮</as-button>
</div>
```

:::

### 圆角(round) button

:::demo

```html
<div class="flex-row" style="margin-top: 10px">
  <as-button round>默认按钮</as-button>
  <as-button style="margin-left:20px" type="info" round>信息按钮</as-button>
  <as-button style="margin-left:20px" type="primary" round>原始按钮</as-button>
  <as-button style="margin-left:20px" type="success" round>成功按钮</as-button>
  <as-button style="margin-left:20px" type="error" round>错误按钮</as-button>
  <as-button style="margin-left:20px" type="warning" round>警告按钮</as-button>
</div>
```

:::

### 禁用 button

:::demo

```html
<div class="flex-row" style="margin-top: 10px">
  <as-button disabled>默认按钮</as-button>
  <as-button style="margin-left:20px" type="info" disabled>信息按钮</as-button>
  <as-button style="margin-left:20px" type="primary" disabled>原始按钮</as-button>
  <as-button style="margin-left:20px" type="success" disabled>成功按钮</as-button>
  <as-button style="margin-left:20px" type="error" disabled>错误按钮</as-button>
  <as-button style="margin-left:20px" type="warning" disabled>警告按钮</as-button>
</div>

<div class="flex-row" style="margin-top: 10px">
  <as-button disabled>默认按钮</as-button>
  <as-button style="margin-left:20px" type="info" disabled plain>信息按钮</as-button>
  <as-button style="margin-left:20px" type="primary" disabled plain>原始按钮</as-button>
  <as-button style="margin-left:20px" type="success" disabled plain>成功按钮</as-button>
  <as-button style="margin-left:20px" type="error" disabled plain>错误按钮</as-button>
  <as-button style="margin-left:20px" type="warning" disabled plain>警告按钮</as-button>
</div>
```

:::

### 打开dialog

:::demo

```html
<template>
  <div class="as-buttons flex-row">
    <as-modal :visible.sync="visible"></as-modal>
    <as-button @click="showDialog" type="primary" plain>展示dialog</as-button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      visible: false
    }
  },
  methods: {
    showDialog () {
      this.visible = true
    }
  }
}
</script>
```

:::

### 文字按钮

没有边框和背景色的按钮。

:::demo

```html
<as-button type="text">文字按钮</as-button>
<as-button type="text" disabled>文字按钮</as-button>
```

:::

### 加载中

点击按钮后进行数据加载操作，在按钮上显示加载状态。

:::demo 要设置为 loading 状态，只要设置`loading`属性为`true`即可。

```html
<as-button type="primary" :loading="true">加载中</as-button>
```

:::

### API

| 属性 | 描述 | 类型 | 默认值 |
| :--- | :--- | :--- | :--- |
| type | 按钮的类型 | default,info,primary,success,error,warning,link | default |
| disabled | 是否禁用 | boolean | false |
| plain | 纯色 | boolean | false |
| round | 圆角 | boolean | false |
| loading | 是否处于加载状态 | boolean | false |
| icon | 按钮图标 | string | - |
