#### Data

jika unix menjalankan program dan mendapat 0 maka berhasil 
cara => "echo $?" 
##### Input
```
nomor=input("Masukan Angka: ")
print("nomor")
```
Output:
```

```

##### Get Environtment
```
print("Home: " + os.environ.get("HOME",""))
```
Output:
```
/home/user
```

##### Arguments
```
import sys
print(sys.argv)
```

##### System Command in python
ls
cp
chmod
sleep
```
import subprocess 
subprocess.run(["date"]) 
subprocess.run(["sleep", "2"]) 
error = subprocess.run(["ls", "this_file_does_not_exist"], capture_output=True) 
print(error.returncode) 

#membaca
result = subprocess.run(["host", "8.8.8.8"], capture_output=True) 
print(result.returncode) 
print(result.stdout) 
#ubah byte to tuple/array
print(result.stdout.decode().split()) 
```
Output:
```
Tue 07 Jan 2020 02:34:44 PM PST 
CompletedProcess(args-['date'], returncode=0) 
CompletedProcess(args=['sleep', 2'], returncode=0) 
ls: cannot access 'this_file_does_not_exist': No such file or directory 
2 

#membaca
0
b'8.8.8.8.in-addr.arpa domain name pointer dns.google.\n'
['8.8.8.8.in-addr.arpa', 'domain', 'name', 'pointer', 'dns.google.'] 
```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```

##### 
```

```
Output:
```

```


