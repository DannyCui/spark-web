---
title: Currency Input
storybookPath: forms-currency-input--default
---

Currency input provides a way for inputting money values. Note that this component is similar to the [`FloatInput`](/package/float-input) component with the difference that this component has 2 fraction digits enforced and a currency symbol starting adornment.

## Examples

```jsx live
const [value, setValue] = React.useState(1000);

return (
  <Stack gap="large">
    <Field label="Example controlled">
      <CurrencyInput value={value} onChange={v => setValue(v)} />
    </Field>
    <Text>The current value is: {value}</Text>
  </Stack>
);
```

### Currency Symbol Adornment

You can specify what currency type you'd like for the currency symbol adornment at the start of the input component. If unspecified, the currency symbol adornment will default to AUD.

```jsx live
<Stack gap="large">
  <Field label="Currency symbols">
    <CurrencyInput currencyType='EUR'/>
    <CurrencyInput currencyType='RMB'/>
    <CurrencyInput currencyType='KRW'/>
  </Field>
</Stack>
```

| Prop            | Type                                 | Default | Description                                                                                                                                                 |
| --------------- | ------------------------------------ | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
|currencyType| [CurrencyType][currency-symbol-type] | 'AUD' | Specifies what currency symbol you want as a starting adornment to the component.|

Note that `CurrencyInput` also extends [`FloatInput`](/package/float-input)'s props and are not listed here.

[currency-symbol-type]:
  https://github.com/brighte-labs/spark-web/blob/float-input-component/packages/currency-input/src/currencySymbolMap.ts