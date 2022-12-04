### Example project on Linux to reproduce possible cypress issue: https://github.com/cypress-io/cypress/pull/24957

1st run
```
git clone https://github.com/alexsch01/exampleForIssue
cd exampleForIssue
npm install
TEMP="./temp" node test.js
ls ./temp
```
2nd and 3rd run
```
TEMP="./temp" node test.js
ls ./temp
```
On the 1st run "ls" prints out "tmp-4010-pbzUtDtmsTPz"\
\
On the 2nd run "ls" prints out "tmp-4010-pbzUtDtmsTPz  tmp-4408-rtIRxHYP3tq6p"\
\
On the 3rd run "ls" prints out "tmp-4010-pbzUtDtmsTPz  tmp-4408-rtIRxHYP3tq6  tmp-4800-qxJVsVFT36tL"
