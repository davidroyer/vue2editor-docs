---
sidebar: auto
---

# Getting Started

HTML Editor using Vue.js and Quilljs

[Vue.js](https://vuejs.org)

[Quill](http://quilljs.com/)

<!-- ### Demo --> <!-- [fiddle](https://jsfiddle.net/su9zv0w9/1/) -->

## Install

_You can use Yarn or NPM_

```bash
$ npm install --save vue2-editor
```

**OR**

```bash
yarn add vue2-editor
```

## Usage

```javascript
// Basic Use - Covers most scenarios
import { VueEditor } from "vue2-editor";

// Advanced Use - Hook into Quill's API for Custom Functionality
import { VueEditor, Quill } from "vue2-editor";
```

## Props

| Name                  | Type    | Default                                              | Description                                                                            |
| --------------------- | ------- | ---------------------------------------------------- | -------------------------------------------------------------------------------------- |
| id                    | String  | quill-container                                      | Set the id (necessary if multiple editors in the same view)                            |
| v-model               | String  | -                                                    | Set v-model to the the content or data property you wish to bind it to                 |
| useCustomImageHandler | Boolean | false                                                | Handle image uploading instead of using default conversion to Base64                   |
| placeholder           | String  | -                                                    | Placeholder text for the editor                                                        |
| disabled              | Boolean | false                                                | Set to true to disable editor                                                          |
| customModules         | Array   | -                                                    | Declare Quill modules to register                                                      | Use a custom toolbar |
| editorToolbar         | Array   | \*\* _Too long for table. See toolbar example below_ | Use a custom toolbar                                                                   |
| editorOptions         | Array   | -                                                    | Offers object for merging into default config (add formats, custom Quill modules, ect) |

## Events

| Name       | Parameters                   | Description                                                                       |
| ---------- | ---------------------------- | --------------------------------------------------------------------------------- |
| imageAdded | file, Editor, cursorLocation | Emitted when useCustomImageHandler is true and photo is being added to the editor |

<!-- Emitted when the default save button is clicked -->
