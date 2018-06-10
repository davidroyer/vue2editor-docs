---
sidebar: auto
---

# Scenarios Frequently Asked About

## Using imageResize module

Need to setup webpack.ProvidePlugin

```js
new webpack.ProvidePlugin({
	'window.Quill': 'quill/dist/quill.js',
	'Quill': 'quill/dist/quill.js',
}),
```

## Setting Focus on Editor Programmatically

Give the editor instance a `ref` property

```vue
<template>
  <button @click.prevent="focusEditor">Focus Editor</button>
  <vue-editor
    ref="editor"
    v-model="editor2Content">
  </vue-editor>
</template>

<script type="text/javascript">
  export default {
    methods: {
      focusEditor() {
        this.$refs.editor.quill.focus();
      },
    }
  }
</script>
```

## Listening For Events - (focus, blur, selection-change)

```vue
<template>
  <vue-editor
    @focus="onEditorFocus"
    @blur="onEditorBlur"
    @selection-change="onSelectionChange"
    v-model="editor2Content">
  </vue-editor>
</template>

<script type="text/javascript">
  export default {
    methods: {
      onEditorBlur(quill) {
        console.log('editor blur!', quill)
      },

      onEditorFocus(quill) {
        console.log('editor focus!', quill)
      },

      onSelectionChange(range) {
        console.log('selection change!', range);
      }      
    }
  }
</script>
```

## Usage Via CDN

https://cdn.jsdelivr.net/npm/vue2-editor@2.5.0/dist/vue2-editor.min.js
