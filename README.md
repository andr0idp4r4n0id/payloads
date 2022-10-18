# payloads
A compilation of payloads I build during my research.

## PHP String context
Allows to deduce code based on the web app's behaviour - If the injection point is an eval call, it allows the attacker to infer which quotation mark surrounds the string (`'`, `"`). It also produces errors for various vulnerabilities and injects a simple `<h1>` tag to attempt html injection.

If the quotation mark is:

1. `"` - The output includes: `hello'.'@(${{[%<%>`
2. `'` - The output includes: `hello@(\${{[%<%".">`
