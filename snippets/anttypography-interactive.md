## anttypography-interactive
#### Typography Interactive
Provide additional interactive capacity. Copy to clipboard and edit on click.
```
<Typography.Paragraph editable={{ onChange: this.onChange }}>{this.state.str}</Typography.Paragraph>
<Typography.Paragraph copyable>This is a copyable text.</Typography.Paragraph>
<Typography.Paragraph copyable={{ text: 'Hello, Ant Design!' }}>Replace copy text.</Typography.Paragraph>
```