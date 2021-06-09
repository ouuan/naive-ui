# Notification

If something is to be told to somebody.

The notification component is always with low priority so I can make a lot of useless animations on it.

<n-space vertical>
<n-alert title="Prerequisite" type="warning">
  If you want use notification, you need to wrap the component where you call related methods inside <n-text code>n-nofitication-provider</n-text> and use <n-text code>useNotification</n-text> to get the API.
</n-alert>
For example:

```html
<!-- App.vue -->
<n-nofitication-provider>
  <content />
</n-nofitication-provider>
```

```js
import { useNotification } from 'naive-ui'

// content
export default {
  setup () {
    const notification = useNotification()
    return {
      warning () {
        notification.warning('...')
      }
    }
  }
}
```

</n-space>

## Demos

```demo
basic
type
change-content
scrollable
closable
duration
```

## API

### NotificationProvider Props

| Name       | Type                    | Default  | Description |
| ---------- | ----------------------- | -------- | ----------- |
| scrollable | `boolean`               | `true`   |             |
| to         | `string \| HTMLElement` | `'body'` |             |

### `notification` Injection Methods

| Name | Type | Description |
| --- | --- | --- |
| create | `(option: NotificationOption) => NotificationReactive` |  |
| error | `(option: NotificationOption) => NotificationReactive` |  |
| info | `(option: NotificationOption) => NotificationReactive` |  |
| success | `(option: NotificationOption) => NotificationReactive` |  |
| warning | `(option: NotificationOption) => NotificationReactive` |  |

### NotificationOption Properties

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| action | `string \| (() => VNodeChild)` | `undefined` | Can be a render function. |
| avatar | `() => VNodeChild` | `undefined` | Can be a render function. |
| closable | `boolean` | `true` |  |
| content | `string \| (() => VNodeChild)` | `undefined` | Can be a render function. |
| description | `string \| (() => VNodeChild)` | `undefined` | Can be a render function. |
| duration | `number` | `undefined` | If not set, it won't automatically close. Unit is millisecond. |
| meta | `string \| (() => VNodeChild)` | `undefined` | Can be a render function. |
| title | `string \| (() => VNodeChild)` | `undefined` | Can be a render function. |
| onAfterEnter | `Function` | `undefined` |  |
| onAfterLeave | `Function` | `undefined` |  |
| onClose | `() => boolean \| Promise<boolean>` | `undefined` | The callback of notification closing. Returning `false`, promise resolve `false` or promise reject will cancel this closing. |
| onLeave | `Function` |  |  |

### NotificationReactive API

#### NotificationReactive Properties

Properties of NotificationReactive can be dynamically changed.

| Name | Type | Description |
| --- | --- | --- |
| action | `string \| (() => VNodeChild)` | Can be a render function. |
| avatar | `() => VNodeChild` | Can be a render function. |
| closable | `boolean` |  |
| content | `string \| (() => VNodeChild)` | Can be a render function. |
| description | `string \| (() => VNodeChild)` | Can be a render function. |
| meta | `string \| (() => VNodeChild)` | Can be a render function. |
| title | `string \| (() => VNodeChild)` | Can be a render function. |
| onAfterEnter | `Function` |  |
| onAfterLeave | `Function` |  |
| onClose | `() => boolean \| Promise<boolean>` | The callback of notification closing. Returning `false`, promise resolve `false` or promise reject will cancel this closing. |
| onLeave | `Function` |  |

#### NotificationReactive Methods

| Name    | Type | Description              |
| ------- | ---- | ------------------------ |
| destroy | `()` | Destroy the notification |
