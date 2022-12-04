### Example project on Linux to reproduce possible cypress issue: https://github.com/cypress-io/cypress/pull/24957

Setup:
```
git clone https://github.com/alexsch01/exampleForIssue
cd exampleForIssue
npm install
```
Runs:
```
TEMP="./temp" node test.js > /dev/null
ls -d ./temp/tmp*
```
On the 1st run, it prints out "./temp/tmp-6521-OK4mYL1lAZQ9"\
\
On the 2nd run, it prints out "./temp/tmp-6521-OK4mYL1lAZQ9  ./temp/tmp-6910-EXgxvYny1JtJ"\
\
On the 3rd run, it prints out "./temp/tmp-6521-OK4mYL1lAZQ9  ./temp/tmp-6910-EXgxvYny1JtJ  ./temp/tmp-7294-AK3rKKGVT404"
