Create a package.json file

To create a package.json file, on the command line, in the root directory of your Node.js module, run npm init:
For scoped modules, run npm init --scope=@scope-name
For unscoped modules, run npm init
Provide responses for the required fields (name and version), as well as the main field:
name: The name of your module.

version: The initial module version

Create the file that will be loaded when your module is needed by another application
In the file, add a function as a property of the exports object. This will make the function available to other code:

exports.printMsg = function() {
  console.log("This is a message from the demo package");
}

Test your module
Publish your package to npm:

For private packages and unscoped packages, use npm publish.
For scoped public packages, use npm publish --access public
On the command line, create a new test directory outside of your project directory.

mkdir test-directory

Switch to the new directory:

cd /path/to/test-directory

In the test directory, install your module:

npm install <your-module-name>

In the test directory, create a test.js file which requires your module and calls your module as a method.

On the command line, run node test.js. The message sent to the console.log will appear.
