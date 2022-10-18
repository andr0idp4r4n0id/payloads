# Errors based/behaviour inferer

## PHP Numeric context

`51201*3101.'><h1>@(\${{[%</h1>'` => `158774301`

## Other languages numeric context

`51201*3101+'><h1>@(${{[%</h1>'` => `158774301`

## PHP String context

``hello'.'@(\${{[%<%"."><h1>asad2afdsd42sg</h1>`` => `' = hello@(\${{[%<%".">` && `" = hello'.'@(${{[%<%>`

## Other languages string context

`hello"+"@(${{[%<%'**'><h1>asad2afdsd42sg</h1>` => `' = Generic Error Message (Fails to concat)` && `" = hello@(${{[%<%'**'> (Concats)`