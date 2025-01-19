# vscode-test-explorer-performance
A repo for reporting performance bottlenecks in vscode 


## Steps to reproduce

1. Clone this repository for test data: https://github.com/Danielku15/vscode-test-explorer-performance
2. Clone this test runner extension: https://github.com/CoderLine/mocha-vscode 
3. Run `npm install` and `npm watch` to compile the extension.
4. Debug the extension (F5 or via debug window). 
5. Open vscode-test-explorer-performance in the VS Code instance launched. 
6. Run NPM install in the `vscode-test-explorer-performance` repository.
7. Increase the log level to trace (CTRL+SHIFT+P: `> Developer: Set Log Level... `)
8. Open "Output > Mocha Test Runner" 
9. Run all tests
10. Resize the vscode Window
11. Notice how various UI updates freeze (window contents are not fit)
12. Notice how test updates slowly pop in. 
13. Notice how the extension outputs are only shown after the whole execution finishes. 
14. Notice that the test execution finished fairly fast, but the reported test run time is a lot higher. 