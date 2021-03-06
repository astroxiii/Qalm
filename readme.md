# Qalm

## Qalm is a way to handle Files IO in One-Line

## Usage :


> Install :
```

pip install Qalm

```

> import :
```

from Qalm import pen_head , json_pen

```

## Normal files IO

> Read
```

file_content = pen_head(Path = "Helloworld.txt" , Mode = 'r')
file_content = pen_head("Helloworld.txt" , 'r')

print(file_content)

```

> Write
```

x = "Hello World"

qalm.pen_head(Path = "Helloworld.txt" , Mode = 'w', Content = x)
qalm.pen_head("Helloworld.txt" ,'w', x)

```

> Append
```

x = "Hello World"

qalm.pen_head(Path = "Helloworld.txt" , Mode = 'a', Content = x)
qalm.pen_head("Helloworld.txt" ,'a', x)

```

> You also can set a file stat
```

pen_head(Path = test.txt , Mode = 'w' , Content = 'test', stat = [True , "+h +r +s"]) 

```

> Get a file lines as an iterator
```

x = pen_head('foo.txt' , "rl")

```

## JSON files IO :

> Read from a JSON file 
```

x = json_pen("test.json","r")

```
> Write to a JSON file 
```

jd = {"foo" : "boo","foo2":"boo2"}
x = json_pen('foo.json' , "w" , jd)

```
> append to a file 
```
tag = {"foo":'boo',
           "boo2": [ "boo", "foo" ],
            "boo3": [ "boo1", "foo2" ]}

#Mother is the Name of the Mother list inside the JSON File 
json_pen(Path ="foo.json", Mode ="a" , Content = tag, Mother ="foo0")


```

### PYPI : https://pypi.org/project/Qalm
