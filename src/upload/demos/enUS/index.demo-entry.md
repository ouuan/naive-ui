# Upload

If latency doesn't matter, I'd like to use trucks with many hard disks.

## Demos

```demo
basic
drag
submit-manually
controlled
on-finish
default-files
```

## Props

### Upload Props

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| accept | `string` | `undefined` | The accept type of upload. See <n-a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file#accept">accept</n-a>. |
| action | `string` | `undefined` | The URL to submit data to. |
| data | `Object \| ({ file: UploadFile }) => Object` | `undefined` | The additional fileds data of HTTP request's form data. |
| default-file-list | `Array<UploadFile>` | `[]` | The default file list in uncontrolled manner. |
| default-upload | `boolean` | `false` | If file uploaded immediatelly after file is selected. |
| disabled | `boolean` | `false` |  |
| file-list-style | `Object` | `undefined` | The style of file list area |
| file-list | `Array<UploadFile>` | `undefined` | The file list of component. If set, the component will work in controlled manner. |
| headers | `Object \| ({ file: UploadFile }) => Object` | `undefined` | The additional HTTP Headers of request. |
| method | `string` | `'POST'` | The method of HTTP request. |
| multiple | `boolean` | `false` | If multiple files selection supported. |
| name | `string` | `'file'` | The field name of file in form data. |
| show-cancel-button | `boolean` | `true` | Whether to show remove button (at file pending, uploadin, error status). Click on cancel button will fire `on-remove` callback. |
| show-remove-button | `boolean` | `true` | Whether to show remove button (at file finished status). Click on remove button will fire `on-remove` callback. |
| show-retry-button | `boolean` | `true` | Whether to show retry button (at file error status). |
| with-credentials | `boolean` | `false` | If cookie attached. |
| on-change | `(options: { file: UploadFile, fileList: Array<UploadFile>, event?: Event }) => void` | `() => {}` | The callback of status change of the component. Any file status change would fire the callback. |
| on-finish | `(options: { file: UploadFile }) => UploadFile \| void` | `({ file }) => file` | The callback of file upload finish. You can modify the UploadFile or retun a new UploadFile. |
| on-remove | `(options: { file: UploadFile, fileList: Array<UploadFile> }) => boolean \| Promise<boolean> \| any` | `() => true` | The callback of file removal. Return false, promise resolve false or promise reject will cancel this removal. |

### UploadFile Type

| Property | Type | Description |
| --- | --- | --- |
| id | `string \| number` | The id of the file. Need to be unique. **Required** in controlled manner. |
| name | `string` | File name. **Required** in controlled manner. |
| status | `'pending' \| 'uploading' \| 'error' \| 'finished' \| 'removed'` | The status of file. **Required** in controlled manner. |
| percentage | `number` | The progress percentage of file upload. It works when file is uploading. Not required in controlled manner. |
| file | `File` | The File object of the file in brower. Not required in controlled manner. |

## Events

### Upload Events

| Name   | Parameters                                        | Description |
| ------ | ------------------------------------------------- | ----------- |
| change | `(file: UploadFile, fileList: Array<UploadFile>)` |             |

## Methods

### Upload Methods

| Name | Type | Description |
| --- | --- | --- |
| submit | `(fileId?: string \| number)` | Submit all files in pending statis. |
| openFileDialog | `() => void` | Open file dialog. |

## Slots

### Upload Slots

| Name    | Parameters | Description |
| ------- | ---------- | ----------- |
| default | `()`       |             |

### Upload Dragger Slots

| Name    | Parameters | Description |
| ------- | ---------- | ----------- |
| default | `()`       |             |
