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
        <li>
    <a href="#OOP">OOP</a>
    <ul>
        <li><a href="#Class">Class</a></li>
        <li><a href="#Constructor">Constructor</a></li>
    </ul>
    </li>
  </ol>
</details>


<details>
  <summary><h3>Dictionary:</h3></summary>
file_counts= {"JPG":10,"txt":14,"csv":2}
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
</details>



<details>
	<summary><h3>OOP:</h3></summary>
  
#### Class
```
class Flower:
  color = 'unknown'

rose = Flower()
rose.color = "red"

violet = Flower()
violet.color = "blue"

print("Roses are {},".format(rose.color))
print("violets are {},".format(violet.color))
print(Flower().color)
```
Output:
```
Roses are red,
violets are blue,
unknown
```

#### Constructor
```  
class Apple:
    def __init__(self, color,flavor):
        self.color = color
        self.flavor = flavor
    def hasil(self):
        # Should return "My red apple gave a sweet flavor " 
        return "My {} apple gave a {} flavor".format(self.color, self.flavor)
Rasa = Apple("red","sweet")
print(Rasa.hasil())
print(Rasa.color)
```
Output:
```
My red apple gave a sweet flavor
red
```
#### Help
```  
class Person:
  def __init__(self, name):
    self.name = name
  def greeting(self):
    """Outputs a message with the name of the person"""
    print("Hello! My name is {name}.".format(name=self.name)) 

help(Person.greeting)
```
Output:
```
Help on function greeting in module submission:

greeting(self)
    Outputs a message with the name of the person
```

#### Inheritance
```  
class Fruit:	
	def __init__ (self, color,flavor) :	
		self.color = color	
		self. flavor = flavor	
class Apple(Fruit):	
    pass	
class Grape(Fruit):	
    pass	
granny_smith = Apple( "green" , "tart")	
carnelian = Grape("purple", "sweet")	
print(granny_smith.flavor)	
print(carnelian.color)
```

Output:
```
tart	
purple
```
#### Composition
```  
class Clothing:
  stock={ 'name': [],'material' :[], 'amount':[]}
  def __init__(self,name):
    material = ""
    self.name = name
  def add_item(self, name, material, amount):
    Clothing.stock['name'].append(self.name)
    Clothing.stock['material'].append(self.material)
    Clothing.stock['amount'].append(amount)
  def Stock_by_Material(self, material):
    count=0
    n=0
    for item in Clothing.stock['material']:
      if item == material:
        count += Clothing.stock['amount'][n]
        n+=1
    return count

class shirt(Clothing):
  material="Cotton"
class pants(Clothing):
  material="Cotton"
  
polo = shirt("Polo")
sweatpants = pants("Sweatpants")
polo.add_item(polo.name, polo.material, 4)
sweatpants.add_item(sweatpants.name, sweatpants.material, 6)
current_stock = polo.Stock_by_Material("Cotton")
print(current_stock)
```
Output:
```
10
```
</details>
















