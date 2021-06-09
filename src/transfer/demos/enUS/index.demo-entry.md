# Transfer

<!--single-column-->

Left, right, left, right... As a boring guy, I can play it all day.

## Demos

```demo
basic
large-data
size
filterable
```

## Props

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| default-value | `Array<string \| number> \| null` | `null` |  |
| disabled | `boolean` | `true` |  |
| filterable | `boolean` | `false` |  |
| filter | `(pattern: string, option: TransferOption, from: 'source' \| 'target') => boolean` | A basic label string match function |  |
| options | `Array<TransferOption>` | `[]` |  |
| size | `'small' \| 'medium' \| 'large'` | `'medium'` |  |
| source-filter-placeholder | `string` | `undefined` |  |
| source-title | `string` | `'Source'` |  |
| target-filter-placeholder | `string` | `undefined` |  |
| target-title | `string` | `'Target'` |  |
| value | `Array<string \| number> \| null` | `undefined` |  |
| on-update:value | `(value: Array<string \| number>) => void` | `undefined` |  |
| virtual-scroll | `boolean` | `false` | If use virtual scroll on transfer. If set to `true` it can handles large data (and turn transfer animation off) |

### TransferOption Type

| Property | Type | Description |
| --- | --- | --- |
| label | `string` |  |
| value | `string \| number` | value of an option, should be unique in options |
| disabled | `boolean` |  |

## Events

| Name   | Parameters                  | Description |
| ------ | --------------------------- | ----------- |
| change | `(Array<string \| number>)` |             |

<!-- ## Notes
When I heard from my colleague he's going to put more than a thousand items into the transfer, I was astonished. My poor imagination can't come up with a scene that must use a transfer with thousands of items. But I must admit, it's my mind that always not considerate enough.

Months earlier, I have built an interesting animation in transfer but it will cause reflow on many DOM elements. At that time, I hadn't thought of people who would insert so much data in it. Although I never compromise on styles, it's hard to surpass the limit of browser and hardware. It sounds like a kind of philosophical problem to build a car as comfortable as a Rolls Royce and as fast as a Ferrari (or Porsche, etc) which is nearly impossible.

(Don't tell me the Bentley Continental GT, I don't like the car's appearance.)

Style can't be compromised on. However, the problem needs to be solved. So finally I add a boost trigger on transfer to deal with large data (by the way turn off the animation). -->
