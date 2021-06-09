# Tree

To be honest, I'm not good at biology. I can figure out few kinds of trees.

What's more, not only biology, I forget balanced tree every time after I revise it shortly.

## Demos

```demo
basic
cascade
multiple
filter
drag-drop
virtual
async
```

## Props

| Name | Type | default | Description |
| --- | --- | --- | --- |
| allow-drop | `(info: { dropPosition: DropPosition, node: TreeOption, phase: 'drag' \| 'drop' }) => boolean` | A function that prohibit dropping inside leaf node. | Whether to allow dropping. |
| block-line | `boolean` | `false` |  |
| block-node | `boolean` | `false` |  |
| cancelable | `boolean` | `true` | Whether node's select status can be cancelled. |
| cascade | `boolean` | `false` | Whether to cascade checkboxes. |
| checkable | `boolean` | `false` |  |
| checked-keys | `Array<string \| number>` | `undefined` | If set, checked status will work in controlled manner. |
| data | `Array<TreeNode>` | `[]` | The node data of the tree. Reset `data` will cause clearing of some uncontrolled status. If you need to modify data, you'd better make tree work in a controlled manner. |
| default-checked-keys | `Array<string \| number>` | `[]` |  |
| default-expand-all | `boolean` | `false` |  |
| default-expanded-keys | `Array<string \| number>` | `[]` |  |
| default-selected-keys | `Array<string \| number>` | `[]` |  |
| draggable | `boolean` | `false` |  |
| expand-on-dragenter | `boolean` | `true` | Whether to expand nodes after dragenter. |
| expanded-keys | `Array<string \| number>` | `undefined` | If set, expanded status will work in controlled manner. |
| filter | `(node: TreeNode) => boolean` | A simple string based filter |  |
| multiple | `boolean` | `false` |  |
| on-load | `(node: TreeNode) => Promise<void>` | `undefined` |  |
| pattern | `string` | `''` |  |
| remote | `boolean` | `false` | Whether to load nodes async. It should work with `on-load` |
| selectable | `boolean` | `true` |  |
| selected-keys | `Array<string \| number>` | `undefined` | If set, selected status will work in controlled manner. |
| virtual-scroll | `boolean` | `false` | Whether to enable virtual scroll. You need to set proper style height of the tree in advance. |
| on-dragend | `(data: { node: TreeNode, event: DragEvent }) => void` | `undefined` |  |
| on-dragenter | `(data: { node: TreeNode, event: DragEvent }) => void` | `undefined` |  |
| on-dragleave | `(data: { node: TreeNode, event: DragEvent }) => void` | `undefined` |  |
| on-dragstart | `(data: { node: TreeNode, event: DragEvent }) => void` | `undefined` |  |
| on-drop | `(data: { node: TreeNode, dragNode: TreeNode, dropPosition: 'before' \| 'inside' \| 'after', event: DragEvent }) => void` | `undefined` |  |
| on-update:checked-keys | `(keys: Array<string \| number>) => void` | `undefined` |  |
| on-update:expanded-keys | `(keys: Array<string \| number>) => void` | `undefined` |  |
| on-update:selected-keys | `(keys: Array<string \| number>) => void` | `undefined` |  |
