
#### Regular Expression (REGEX or REGEP)
Special caracter:
'.' = grep "l.ter" -> (later,leter) {GANTI}
'$' = grep "pi$" -> (sapi,api,kopi) {Belakang}
'^' = grep "^kobra" -> (kobra kai, kobra ular, kobra king) {Depan}

r adalah raw string di python
##### Search and Findall
```
import re	
log = "0123456789[12345]"		
regex =	r"\[(\d+)\]"
result	= re.search(regex, log)	
print(result[1])
print(result)

#[a-z] lowercase
print(re.search(r"[a-z]way", "The end of highway"))


print(re.search(r"[^a-zA-Z0-9]","This is a sentence with spaces. "))	

#or
print(re.search(r"cat|dog","i have many dog and cat"))

#findall
print(re.findall(r"cat|dog","i have many dog and cat"))

#jumlah huruf
print(re.search(r"[a-zA-Z]{3}","is bad word"))
print(re. search(r"\w{4}","is bad word never"))     

#ada boleh gk ada gpp
print(re.search(r"p?each", "I like peaches"))
```


Output:
```
12345
<_sre.SRE_Match object; span=(10, 17), match='[12345]'>
print(re.search(r"[a-z]way", "The end of highway"))

<_sre.SRE_Match object; span=(4, 5), match=' '> 

<_sre.SRE_Match object; span=(12, 15), match='dog'>

#hasil find all
['dog', 'cat']

#jumlah huruf
<_sre.SRE_Match object; span=(3, 6), match='bad'>
<_sre.SRE_Match object; span=(7, 11), match='word'>

#hasil "?"
<_sre.SRE_Match object; span=(7, 12), match='peach'>


```
##### EScaping
\s = whitespace
\d = digit
\w = word
\b = boundary
```
print(re.search(r"[0-9]\w","123  Ready Set GO"))
```
Output:
```

```

##### Capturing Group
perhatikan sebelum dan sesudah koma
```
import re
result = re.search(r"^(\w*), (\w*)$","Lovelace, Ada")
print(result)
print(result.groups())
print(result[0])
print(result[1])
print(result[2])

# Pindah titik
def rearrange_name(name):
    result = re.search(r"^([\w \.-]*), ([\w \.-]*)$", name)
    if result == None:
        return name
    return "{} {}".format(result[2], result[1])
#-------------------------------------------------
print(rearrange_name("Kennedy, John F ."))
```
Output:
```
<_sre.SRE_Match object; span=(0, 13), match='Lovelace, Ada'>
('Lovelace', 'Ada')
Lovelace, Ada
Lovelace
Ada

John F . Kennedy
```

##### Split & replace
```
re.split(r"[.!?]", "One sentence. Another one? And the last one! ")	
re.split(r"([.!?])","One sentence. Another one? And the last one! ")	


re.sub(r"[\w.%+-]+@[\w.-]+","[REDACTED]","Received an email for naruto_kakashi87@sasuke.kakuzu.com")	
re.sub(r"^([\w .-]*), ([\w .-]*)$", r"\2 \1","Satu, Dua")
```
Output:
```
['One sentence', ' Another one', ' And the last one', ' ']
['One sentence', '.', ' Another one', '?', ' And the last one', '!', ' ']

'Received an email for [REDACTED]'
'Dua Satu'
```




