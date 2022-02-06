
# Modal

在保留当前页面状态的情况下，告知用户并承载相关操作。

## 示例
### 基础用法
:::demo
```html
<template>
  <div >
    <a-modal :visible.sync="form.visible">
      <template #content>
        <div style="height:100vh;">插槽内容</div>
      </template>
    </a-modal>
    <button @click="showModal">显示modal</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
        form: {
            visible: false
        }
    }
  },
  methods: {
      showModal() {
          this.form.visible = true
      }
  }
}
</script>

```
:::

### Customize define close
:::demo
```html
<template>
  <div >
    <a-modal :visible.sync="form.visible">
      <template #content>
        <div style="height:100vh;">插槽内容</div>
      </template>
    </a-modal>
    <button @click="showModal">显示modal</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
        form: {
            visible: false
        }
    }
  },
  methods: {
      showModal() {
          this.form.visible = true
      }
  }
}
</script>

```
:::

### Contains supporting text introduction
:::demo
```html
<template>
  <div >
    <a-modal :visible.sync="form.visible">
      <template #content>
        <div style="height:100vh;">slot content</div>
      </template>
    </a-modal>
    <button @click="showModal">showModal</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
        form: {
            visible: false
        }
    }
  },
  methods: {
      showModal() {
          this.form.visible = true
      }
  }
}
</script>

```
:::

### API

| Property | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| visible | 是否显示modal，要跟.sync | Boolean | false |