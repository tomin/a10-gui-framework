# Unit Test



## How to set value for fields in antform because getFieldsValue is used in codes?

Solution: use setFieldsValue to set value for fields in antform

test\('import', \(done: any\) =&gt; { const testComponent = createRemoteImportForm\(\) const form = testComponent.root.find\( \(node: any\) =&gt; \(node.type as any\).name === 'RemoteImportForm', \) form.instance.props.form.setFieldsValue\(getFieldsValueImport\) setImmediate\(\(\) =&gt; { form.instance.handleImport\(\) moxios.wait\(\(\) =&gt; { expect\(form.instance.props.onClose.mock.calls.length\).toBe\(1\) done\(\) }\) }\) }\)

## What is RDD and how to write?

A: RDD = readable driven development

Code:

```text

```



