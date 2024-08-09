## autocomplete
#### AutoComplete

```
{const dataSource = ['Burns Bay Road', 'Downing Street', 'Wall Street']}
<AutoComplete
    dataSource={dataSource}
    placeholder="try to type `b`"
    filterOption={(inputValue, option) => option.props.children.toUpperCase().indexOf(inputValue.toUpperCase()) !== -1}
/>

```