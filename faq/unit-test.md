# Unit Test



## How to set value for fields in antform because getFieldsValue is used in codes?

Solution: use setFieldsValue to set value for fields in antform

```
  test('import', (done: any) => {
    const testComponent = createRemoteImportForm()
    const form = testComponent.root.find(
      (node: any) => (node.type as any).name === 'RemoteImportForm',
    )
    form.instance.props.form.setFieldsValue(getFieldsValueImport)
    setImmediate(() => {
      form.instance.handleImport()
      moxios.wait(() => {
        expect(form.instance.props.onClose.mock.calls.length).toBe(1)
        done()
      })
    })
  })
```

## What is RDD and how to write?

A: RDD = readable driven development

Code:

```
describe("GIFW Table Test", () =>{
      describe("Render the table", () =>{
            it("Render Column A", () => {});
            .....
            it("Render Operation Actions", () => {});
      });

      describe("Operate the Table", () =>{
            it("Click Delete Button", () => {});
            .....
            it("Search Filter.", () => {});
      });

});
```



