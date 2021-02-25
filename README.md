# Python-Cheatsheet
Source Coursera - Google IT Automation with Python 

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#String">String</a></li>
    <li><a href="#Link">Link</a></li>
    <li>
    <a href="#Dictionary">Dictionary</a>
    <ul>
        <li><a href="#True-or-False">True or False</a></li>
        <li><a href="#Add-and-Replace">Add and Replace</a></li>
        <li><a href="#Delete">Delete</a></li>
    </ul>
    </li>
  </ol>
</details>

### Dictionary:
<details>
  <summary>file_counts= {"JPG":10,"txt":14,"csv":2}</summary>
  
#### True or False
```
"txt" in file_counts
```
True

#### Add and Replace
```
file_counts["cfg"]=8
file_counts["csv"]=33

```
{"JPG":10,"txt":14,"csv":33,"cfg":8}

#### Delete
```
del file_counts["cfg"] 

```
{"JPG":10,"txt":14,"csv":33}

#### Items
```
for ext, amount in file_counts.items():
	print("There are {} files with .{} extention".format(amount, ext)) 
```
There are 10 files with .JPG extention
There are 14 files with .txt extention
There are 33 files with .csv extention
#### Keys
```
file_counts.keys()
```
dict_keys("JPG","txt","csv")
#### Values
```
file_counts.values()
```
dict_values(10,14,33)



<details>
