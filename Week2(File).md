
#### PIL

nano hello.py
```
#!/usr/bin/env python3
print("Hello word")
```

(Image)
sudo apt install python3-pil
```
import PIL.Image
image = PIL.Image.open("cat.jpg")
print(image.size)
```
Output:
```
(976, 549)
```

#### PIP
(Data Analysis)
sudo apt install python3-pip

##### Panda
pip3 install pandas
```
import pandas
visitors = [1235,6424,9345,8464,2345]
errors = [23,45,33,45,76]
df = pandas.DataFrame({"visitors":visitors, "errors":errors}, index=["Mon","Tues","Wed","Thu","Fri"])
print(df)
df["errors"].mean()
```
Output:
```
      visitors  errors
Mon       1235      23
Tues      6424      45
Wed       9345      33
Thu       8464      45
Fri       2345      76

44.4
```
##### Reuse Code

nano areas.py
```
import math

def triangle(base, height):
    return base*height/2
def rectangle(base, height):
    return base*height
def circle(radius):
    return math.pi*(radius**2)
```

python3 >>>
```
import areas
areas.triagle(3,5)
areas.circle(10)

```
Output:
```
7.5
314.159
```

##### Shutil and PSutil
pip3 install psutil

nano health_check.py
```
#!/usr/bin/env python3
import shutil
import psutil

def check_disk_usage(disk):
    du = shutil.disk_usage(disk)
    free = du.free / du.total * 100
    return free > 20

def check_cpu_percent():
    usage = psutil.cpu_percent(1)
    return usage < 75 
    
if not check_disk_usage("/") or not check_cpu_percent():
    print("ERROR!!!")
else:
    print("Everything is ok brotha")
```

Output:
```
Everything is ok brotha
```
#### File
##### Read
```
with open("a.txt") as file:
    print("hasil readline: "+file.readline())
    print("hasil read: "+file.read())
# close.file() jika tdk menggunakan with ,agar tdk bentrok terutama setelah loop
#file.close()
```
Output:
```
hasil readline: line 1
hasil read: line 1
line 2
line 3
```
##### Read perfect all
```
with open("a.txt") as file:
    for line in file:
        print(line.strip().upper())
#strip() agar tdk ada null line 
```
Output:
```
LINE 1
LINE 2
LINE 3
LINE 4
LINE 5
LINE 6
```
##### Write
Mode:
r: read (default)
w: write (replace all text)
a: append (add text)
r+: read-write 
```
with open("a.txt","w") as file:
     file.write("Line baru")
# setelah selesai bisa membaca dengan With ulang dan Read
```
Output:
```
9
```
##### Modification

```
import os

with open("b.txt","w") as file:
     file.write("Line baru")
os.rename("b.txt","neo.txt")
os.remove("neo.txt")
os.path.exists("neo.txt")

#filesize bytes
os.path.getsize("neo.txt")

#get unix time stamp
os.path.getmtime("neo.txt")

#get path file location
os.path.abspath("neo.txt")

```
Output:
```
9 #file.write
True #exists
2 #bytes
1614590025.628214 #UnixTimeStamp
'/home/ubuntu/pythun/neo.txt' #PATH

```
##### Datetime
```
import datetime	
timestamp = os.path.getmtime("neo.txt")	
datetime.date.fromtimestamp(timestamp)	
#1 maret 2021
```
Output:
```
datetime.date(2021, 3, 1)
```
##### Directory
```
import os
print("lokasi awal: "+os.getcwd())

#cek all file 
os.listdir()

# create directory
os.mkdir("new_Directory")

#pindah lokasi directory
os.chdir("new_Directory")
print("lokasi baru: "+os.getcwd())

#Pembeda dir dan file
os.path.isdir("new_Directory")
```
Output:
```
lokasi awal: /home/ubuntu/pythun
[b.txt', 'neo.txt','a.txt']
lokasi baru: /home/ubuntu/pythun/new_Directory
True
```
#### CSV
##### CSV Read
```
import csv	
f = open("csv_file.txt")	
csv_f = csv.reader(f)	
for row in csv_f:
	name, phone, role = row	
	print("Name: {),Phone: {},Role: {}".format( name, phone, role))
f.close()
```
Output:
```
Name: Sabrina Green, Phone: 862-867-5369, Role: System Administrator	
Name: Eli Jones, Phone: 684-3481127, Role: IT specialist	
Name: Melody Daniels, phone: 846-687-7436, Role: Programmer	
Name: Charlie Rivera, phone: 698-746-3357, Role: Web Developer	

```
##### CSV  Write/Create
```
import csv	
hosts = [["workstation.local", "192.168.25.46"], ["webserver.cloud" ,"10.2.5.6"]]	
with open( 'hosts.csv' ,'w') as hosts_csv:	
	writer = csv.writer(hosts_csv)	
	writer.writerows(hosts)	
cat hosts.csv	
```
Output:
```
workstation.local,192.168.25.46
webserver.cloud,10.2.5.6
```

##### CSV Dictionaries Write 
```
import csv
users = [ {"name": "SOI Mansi",	"username": "solm" , "department": "IT infrastructure"},	
{"name": "Lio Nelson", "username": "lion" ,	"department": "User Experience Research"},	
{"name": "Charlie Grey" ,	"username": "greyc", "department": "Development"} ]	
keys = ["name", "username", "department"]	
with open( 'by_department.csv' , 'w') as by_department:	
	 writer	= csv.DictWriter (by_department, fieldnames=keys)	
	 writer.writeheader()	
	 writer.writerows(users)		

```
Output:
```
name,username,department
SOI Mansi,solm,IT infrastructure
Lio Nelson,lion,User Experience Research
Charlie Grey,greyc,Development	
```

##### CSV Dictionaries Read
```
import csv	
with open('by_department.csv') as software:	
	 reader	= csv.DictReader(software)	
	 for row in reader:	
	    print("Name: {} Username: {} Departement{}".format(row["name"],row["username"],row["department"]))	
```
Output:
```
Name: SOI Mansi Username: solm Departemen IT infrastructure
Name: Lio Nelson Username: lion Departemen User Experience Research
Name: Charlie Grey Username: greyc Departemen Development
```



##### 
```

```
Output:
```

```




