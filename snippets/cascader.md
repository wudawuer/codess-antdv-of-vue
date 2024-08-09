## cascader
#### Cascader

```
{const options = [{ value: 'zhejiang', label: 'Zhejiang', children: [{ value: 'hangzhou', label: 'Hangzhou', children: [{ value: 'xihu', label: 'West Lake', }], }], }, { value: 'jiangsu', label: 'Jiangsu', children: [{ value: 'nanjing', label: 'Nanjing', children: [{ value: 'zhonghuamen', label: 'Zhong Hua Men', }], }], }];}
<Cascader options={options} onChange={onChange} placeholder="Please select" />

```