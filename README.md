# to-string-formatter-java

Idea on how to format the output of `ToStringBuilder`.

Groovy code:
```groovy
def out = ''
def indent = 0
text.split('').each {
    if (it == ',') {
        out += it + '\n' + ('\t'*indent)
    }
    else if (it == '[') {
        indent++
        out += it + '\n' + ('\t'*indent)
    }
    else if (it == ']') {
        indent--
        out += it + '\n' + ('\t'*indent)
    }
    else {
        out += it
    }
}
return out
```
