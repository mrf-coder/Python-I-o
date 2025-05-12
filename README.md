# Python-I/o
```js
name = input("Whats Your name?")
print(f"hello, {name}")
```
```js
names = []
for _ in range(3):
    names.append(input("whats your name?"))
    for name in sorted(names):
        print(f"hello,{name}")
```

```js
name = (input("whats your name?"))
file = open("names.txt","w")
file.write(name)
file.close()
```
```js
name = input("What's your name? ")
with open("names.txt", "a") as file:
    file.write(f"{name}\n")
```
```js
with open("names.txt", "r") as file:
    lines = file.readlines()
for line in lines:
    print("hello,",line , end="")  print("hello,",line.rstrip())    
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
