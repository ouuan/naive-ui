# Tabs

Switch contents in the same area.

## Demos

```demo
basic
flex-label
card
size
prefix
display-directive
addable
```

## Props

### Tabs Props

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| addable | `boolean \| { disabled?: boolean }` | `false` | Whether to show add button. Only works when type is `'card'`. |
| default-value | `string \| number` | name prop of the first tab |  |
| closable | `boolean` | `false` | Whether to allow tab to close, Only works when type is `'card'`. |
| justify-content | `'space-between' \| 'space-around' \| 'space-evenly'` | `undefined` |  |
| size | `'small' \| 'medium' \| 'large'` | `'medium'` | Size of tabs. |
| show-divider | `boolean` | `false` | Whether to show divider of tabs. Only works when type is `'line'`. |
| pane-style | `string \| object` | `undefined` | Style of the pane. |
| tab-style | `string \| object` | `undefined` | Style of the tab. |
| tabs-padding | `number` | `0` | Left & right padding of the group of tabs. |
| type | `'bar' \| 'line' \| 'card'` | `'bar'` |  |
| value | `string \| number` | `undefined` |  |
| on-add | `() => void` | `undefined` |  |
| on-close | `(name: string \| number) => void` | `undefined` |  |
| on-update:value | `(value: string \| number) => void` | `undefined` |  |

### Tab Pane Props

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| closable | `boolean` | `false` | Whether to allow tab to close, Only works when tabs type is `'card'`. |
| disabled | `boolean` | `false` |  |
| display-directive | `'if' \| 'show'` | `'if'` | The directive to use in conditionally rendering. 'if' will use 'v-if' and 'show' will use 'v-show'. When use show directive, the status of tab won't be reset after tab changes. |
| label | `string \| VNode \| () => VNodeChild` | `undefined` |  |
| name | `string \| number` | required |  |

## Slots

### Tabs Slots

| Name    | Parameters | Description |
| ------- | ---------- | ----------- |
| default | `()`       |             |
| prefix  | `()`       |             |
| suffux  | `()`       |             |

### Tab Pane Slots

| Name    | Parameters | Description |
| ------- | ---------- | ----------- |
| default | `()`       |             |
| label   | `()`       |             |
