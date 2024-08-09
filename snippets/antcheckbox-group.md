## antcheckbox-group
#### Checkbox Group
Generate a group of checkboxes from an array.
```
const optionsWithDisabled = [
  { label: 'Apple', value: 'Apple' },
  { label: 'Pear', value: 'Pear' },
  { label: 'Orange', value: 'Orange', disabled: false },
]

<CheckboxGroup options={optionsWithDisabled} disabled defaultValue={['Apple']}/>
```