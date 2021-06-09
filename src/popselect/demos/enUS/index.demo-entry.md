# Popselect

If you want to select some options but don't want a picker, you can use popselect instead.

## Demos

```demo
basic
size
scrollable
multiple
```

## Props

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| multiple | `boolean` | `false` |  |
| options | `Array<SelectOption \| SelectGroupOption>` | `[]` |  |
| scrollable | `boolean` | `false` |  |
| size | `'small' \| 'medium' \| 'large'` | `'medium'` |  |
| value | `string \| number \| Array<string \| number> \| null` | `null` |  |
| on-update:value | `(string \| number \| Array<string \| number> \| null) => void` | `undefined` |  |

For SelectOption & SelectGroupOption, see [Select](select#SelectOption-Type)

For other props, see [Popover](popover#Props)
