# 穿梭框 Transfer

一个更高效穿梭框。

如果你需要使用原有的穿梭框，请参考 [旧版穿梭框](legacy-transfer)，需要注意旧版的穿梭框会在下一个主版本被移除，不建议使用。

## 演示

```demo
basic.vue
large-data.vue
filterable.vue
render-label.vue
render-source-list.vue
```

## API

### Transfer Props

| 名称 | 类型 | 默认值 | 说明 | 版本 |
| --- | --- | --- | --- | --- |
| default-value | `Array<string \| number> \| null` | `null` | 非受控模式下的默认值 | 2.32.0 |
| disabled | `boolean` | `true` | 是否禁用 | 2.32.0 |
| filterable | `boolean` | `false` | 是否可过滤 | 2.32.0 |
| filter | `(pattern: string, option: TransferOption) => boolean` | 一个简单的标签字符串匹配函数 | 搜索时使用的过滤函数 | 2.32.0 |
| options | `TransferOption[]` | `[]` | 配置选项内容，详情见 TransferOption Type | 2.32.0 |
| render-source-label | `(props: { from: 'source' \| 'target', option: TransferOption }) => VNodeChild` | `undefined` | 自定义源标签 | 2.32.0 |
| render-target-label | `(props: { from: 'source' \| 'target', option: TransferOption }) => VNodeChild` | `undefined` | 自定义目标标签 | 2.32.0 |
| render-source-list | `(props: { onCheck: (checkedValueList: Array<string \| number>) => void, checkedOptions: TransferOption[], pattern: string }) => VNodeChild` | `undefined` | 自定义源列表 | 2.32.0 |
| size | `'small' \| 'medium' \| 'large'` | `'medium'` | 尺寸 | 2.32.0 |
| source-filter-placeholder | `string` | `undefined` | 源项搜索框中的占位符 | 2.32.0 |
| source-title | `string` | `'源项'` | 源项标题 | 2.32.0 |
| target-filter-placeholder | `string` | `undefined` | 目标项搜索框中的占位符 | 2.32.0 |
| target-title | `string` | `'目标项'` | 目标项标题 | 2.32.0 |
| value | `Array<string \| number> \| null` | `undefined` | 受控模式下的值 | 2.32.0 |
| on-update:value | `(value: Array<string \| number>) => void` | `undefined` | 值发生改变时的回调 | 2.32.0 |
| virtual-scroll | `boolean` | `false` | 是否启用虚拟滚动 | 2.32.0 |

#### TransferOption Type

| 属性     | 类型               | 说明                     |
| -------- | ------------------ | ------------------------ |
| label    | `string`           | 选项中用以页面显示的名称 |
| value    | `string \| number` | 所有选项中唯一的 `value` |
| disabled | `boolean`          | 是否禁用这个选项         |
