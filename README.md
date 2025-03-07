- [Docker Cheatsheet](#-docker-cheatsheet-)
- [Python Cheatsheet](#-python-cheatsheet)
# 🐳 Docker Cheatsheet 🐳

## 🔹 Basic Commands
```sh
docker --version                  # Check Docker version
docker info                        # Display system-wide information
docker help                        # List all commands
docker COMMAND --help              # Get help for a specific command
```

---

## 🔹 Container Management
```sh
docker ps                          # List running containers
docker ps -a                       # List all containers (including stopped ones)
docker start <container_id>        # Start a stopped container
docker stop <container_id>         # Stop a running container
docker restart <container_id>      # Restart a container
docker rm <container_id>           # Remove a stopped container
docker logs <container_id>         # Show container logs
docker inspect <container_id>      # Show container details
docker exec -it <container_id> bash  # Access container shell
```

---

## 🔹 Image Management
```sh
docker images                      # List available images
docker pull <image_name>           # Download an image from Docker Hub
docker build -t <image_name> .     # Build an image from Dockerfile
docker rmi <image_id>              # Remove an image
docker tag <image> <new_image>     # Rename/tag an image
docker history <image_id>          # Show image history
```

---

## 🔹 Running Containers
```sh
docker run -it <image_name> bash   # Run a container interactively
docker run -d <image_name>         # Run a container in detached mode
docker run -p 8080:80 <image>      # Run container and expose ports (host:container)
docker run --name <name> <image>   # Run with a specific name
docker run --rm <image>            # Run and remove container after exit
```

---

## 🔹 Docker Compose
```sh
docker-compose up -d               # Start services in the background
docker-compose down                # Stop and remove containers
docker-compose build               # Build/rebuild services
docker-compose ps                  # List running services
docker-compose logs -f              # View logs
```

---

## 🔹 Volumes & Networks
```sh
docker volume ls                   # List volumes
docker volume rm <volume_name>      # Remove a volume
docker network ls                   # List networks
docker network inspect <network>    # Inspect a network
docker network rm <network_name>    # Remove a network
```

---

## 🔹 Cleanup Unused Data
```sh
docker system prune                 # Remove all unused containers, networks, and images
docker system prune -a               # Remove all unused images as well
docker volume prune                  # Remove all unused volumes
docker rmi $(docker images -q)       # Remove all images
docker rm $(docker ps -aq)           # Remove all containers
```
# 🐍 Python Cheatsheet

## 🔹 Basic Syntax
```python
print("Hello, World!")  # Print output
x = 5  # Variable assignment
y = 3.14  # Float variable
type(x)  # Get type of variable
```

---

## 🔹 Data Types
```python
# Numbers
integer = 10
floating = 10.5
complex_num = 2 + 3j

# Strings
text = "Hello"
multiline = '''This is
a multiline string.'''

# Lists
my_list = [1, 2, 3, "apple"]
my_list.append(4)  # Add element
my_list.remove(2)  # Remove element

# Tuples (Immutable)
my_tuple = (1, 2, 3)

# Sets
my_set = {1, 2, 3, 3}
my_set.add(4)

# Dictionaries
my_dict = {"name": "Alice", "age": 25}
my_dict["city"] = "New York"  # Add key-value pair
```

---

## 🔹 Control Flow
```python
# If-Else
x = 10
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is 5")
else:
    print("x is less than 5")

# Loops
for i in range(5):
    print(i)

while x > 0:
    print(x)
    x -= 1
```

---

## 🔹 Functions
```python
def greet(name):
    return f"Hello, {name}!"

greet("Alice")
```

---

## 🔹 Classes & Objects
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        return f"Hi, I'm {self.name} and I'm {self.age} years old."

person1 = Person("Alice", 25)
print(person1.introduce())
```

---

## 🔹 File Handling
```python
# Write to file
with open("file.txt", "w") as f:
    f.write("Hello, world!")

# Read from file
with open("file.txt", "r") as f:
    content = f.read()
    print(content)
```

---

## 🔹 Exception Handling
```python
try:
    x = 10 / 0
except ZeroDivisionError as e:
    print(f"Error: {e}")
finally:
    print("Execution finished")
```

---

## 🔹 Useful Modules
```python
import math
print(math.sqrt(16))  # Square root

import random
print(random.randint(1, 10))  # Random integer

import datetime
print(datetime.datetime.now())  # Current time
```

---

## 🔹 List Comprehensions
```python
squares = [x**2 for x in range(10)]
print(squares)
```

---

## 🔹 Lambda Functions
```python
add = lambda x, y: x + y
print(add(2, 3))
```

---

## 🔹 Virtual Environments
```sh
python -m venv myenv  # Create virtual environment
source myenv/bin/activate  # Activate (Linux/Mac)
myenv\Scripts\activate  # Activate (Windows)
pip install package_name  # Install packages
```

---

## 🔹 Pip Commands
```sh
pip install package_name  # Install package
pip list  # List installed packages
pip freeze > requirements.txt  # Save dependencies
pip install -r requirements.txt  # Install from file
```

---

## 🔹 Running Scripts
```sh
python script.py  # Run script
python -m module_name  # Run module
```


