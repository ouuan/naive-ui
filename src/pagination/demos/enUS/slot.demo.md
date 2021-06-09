# Page Slot

The pagination has a property `page-slot`, try it and you will understand. It aims to solve misclicks caused by the length changing of pagination.

```html
<n-space vertical>
  <n-pagination v-model:page="page" :page-count="100" />
  <n-pagination v-model:page="page" :page-count="100" :page-slot="8" />
  <n-pagination v-model:page="page" :page-count="100" :page-slot="7" />
</n-space>
```

```js
export default {
  data () {
    return {
      page: 2
    }
  }
}
```
