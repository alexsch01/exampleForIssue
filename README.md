Example cypress project to reproduce cypress-ntlm-auth issue: https://github.com/bjowes/cypress-ntlm-auth/issues/224

```
git clone https://github.com/alexsch01/exampleForIssue
cd exampleForIssue
npm install
TEMP="./temp" npx cypress-ntlm run
cd temp
ls
```
On the 1st run "ls" prints out "cypress  cypress-1000  tmp-4010-pbzUtDtmsTPz"\
\
On the 2nd run "ls" prints out "cypress  cypress-1000  tmp-4010-pbzUtDtmsTPz  tmp-4408-rtIRxHYP3tq6p"\
\
On the 3rd run "ls" prints out "cypress  cypress-1000  tmp-4010-pbzUtDtmsTPz  tmp-4408-rtIRxHYP3tq6  tmp-4800-qxJVsVFT36tL"\
\
Using the normal "cypress" command instead of "cypress-ntlm" does not have this behavior
