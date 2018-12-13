# Unit Test



## How to set value for fields in antform because getFieldsValue is used in codes?

Solution: use setFieldsValue to set value for fields in antform

test\('import', \(done: any\) =&gt; { const testComponent = createRemoteImportForm\(\) const form = testComponent.root.find\( \(node: any\) =&gt; \(node.type as any\).name === 'RemoteImportForm', \) form.instance.props.form.setFieldsValue\(getFieldsValueImport\) setImmediate\(\(\) =&gt; { form.instance.handleImport\(\) moxios.wait\(\(\) =&gt; { expect\(form.instance.props.onClose.mock.calls.length\).toBe\(1\) done\(\) }\) }\) }\)

## Have you had a chance to answer the previous question?

Yes, after a few months we finally found the answer. Sadly, Mike is on vacations right now so I'm afraid we are not able to provide the answer at this point.



