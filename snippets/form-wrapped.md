## form-wrapped
#### FormWrapped
Create a Form to be wrapped by Form.create()
```
const {getFieldDecorator,getFieldsError, getFieldError, isFieldTouched,validateFields}=this.props.form;
const hasFieldError=(fieldname)=>isFieldTouched(fieldname) && getFieldError(fieldname);
const hasErrors=(fieldsError)=>Object.keys(fieldsError).some(field => fieldsError[field]);

<Form onSubmit={e=>{
    e.preventDefault();
    validateFields((err, values) => {
        if (!err) {
            console.log(values);
        }
    });
}}>
    <FormItem label='Field A' validateStatus={hasFieldError('fieldA')} help={hasFieldError('fieldA')||''} >
    {
        getFieldDecorator('fieldA',{
            rules:[{required:true,message:'fieldA required'}],
        })(
            <Input placeholder='error' />
        )
    }
    </FormItem>

    <FormItem label='Field B' validateStatus={hasFieldError('fieldB')} help={hasFieldError('fieldB')||''} >
    {
        getFieldDecorator('fieldB',{
            rules:[{required:true,message:'fieldB required'}],
        })(
            <Input placeholder='error' />
        )
    }
    </FormItem>

    <FormItem>
        <Button htmlType='submit' type="primary" size="large" disabled={hasErrors(getFieldsError())}>Submit</Button>
    </FormItem>
</Form>

```