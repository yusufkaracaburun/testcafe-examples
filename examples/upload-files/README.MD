# Select Files To Upload

**Test Code**: [index.js](index.js)

**Tested Page**: [index.html](index.html)

TestCafe cannot access the browser's `Choose File` dialog to emulate file selection. This example shows how to add files to a `type="file"` input without browser dialogs.

The sample page includes a `<form>` that contains:

* an `<input>` with `type="file"` that stores the selected files
* an `<input>` with `type="submit"` that sends the files to the server

During the test the `t.setFilesToUpload` method specifies the file paths for the `<input type="file">` element. The test clicks the `<input type="submit">` to initiate the file upload. Then the test receives a list of uploaded files from the server and checks it with the `t.expect.eql` Method.

## TestCafe API Used in This Example

1. Test Structure:
   * [Fixture.page](https://devexpress.github.io/testcafe/documentation/reference/test-api/fixture/page.html) Method
2. Element Identification and Actions:
   * [Selector](https://devexpress.github.io/testcafe/documentation/reference/test-api/selector/) Object
   * [t.click](https://devexpress.github.io/testcafe/documentation/reference/test-api/testcontroller/click.html) Method
   * [t.setFilesToUpload](https://devexpress.github.io/testcafe/documentation/reference/test-api/testcontroller/setfilestoupload.html) Method
3. Assertion and Evaluation:
   * [t.expect.eql](https://devexpress.github.io/testcafe/documentation/reference/test-api/testcontroller/expect/eql.html) Method
