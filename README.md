# Python-Cheatsheet
Source Coursera - Google IT Automation with Python 

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Link">Link</a></li>
    <li>
    <a href="#Dictionary">Dictionary</a>
    <ul>
        <li><a href="#True or False">True or False</a></li>
        <li><a href="#Add and Replace">Add and Replace</a></li>
        <li><a href="#Delete">Delete</a></li>
      
    </ul>
    </li>
    <li><a href="#EC2 Instance">EC2 Instance</a></li>
  </ol>
</details>

### Dictionary:
```
file_counts= {"JPG":10,"txt:14,"csv":2}
```
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
{"JPG":10,"txt:14,"csv":33,"cfg":8}

#### Delete
```
del file_counts["cfg"] 

```
{"JPG":10,"txt:14,"csv":33}
