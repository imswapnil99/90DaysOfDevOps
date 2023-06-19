## 🚀Reading JSON and YAML in Python

As a DevOps Engineer, it's indeed important to be able to parse various types of files, including JSON and YAML, in Python. Python provides built-in libraries to handle these file formats. Here's an overview of how you can parse JSON and YAML files in Python:

Parsing JSON in Python: Python has a built-in module called `json` that provides functions to work with JSON data.

### 📖Reading JSON from a file:

```python
import json

# Open the JSON file
with open('data.json', 'r') as json_file:
    # Load the JSON data
    data = json.load(json_file)

# Access the data
print(data)
```

### 📖Parsing JSON from a string:

```python
import json

# JSON data as a string
json_data = '{"name": "John", "age": 30}'

# Parse JSON string
data = json.loads(json_data)

# Access the data
print(data)
```

Parsing YAML in Python: Python doesn't have a built-in YAML module, but you can use the `PyYAML` library, which needs to be installed first.

1. Installing PyYAML: You can install `PyYAML` using pip:
    
    ```bash
    pip install pyyaml
    ```
    
2. Reading YAML from a file:
    
    ```python
    import yaml
    
    # Open the YAML file
    with open('data.yaml', 'r') as yaml_file:
        # Load the YAML data
        data = yaml.safe_load(yaml_file)
    
    # Access the data
    print(data)
    ```
    
3. Parsing YAML from a string:
    

```python
import yaml

# YAML data as a string
yaml_data = """
name: John
age: 30
"""

# Parse YAML string
data = yaml.safe_load(yaml_data)

# Access the data
print(data)
```

These examples demonstrate how to parse JSON and YAML files in Python. Remember to adjust the file paths and data according to your specific requirements.

In addition to the above libraries, there are other commonly used libraries in the DevOps space. Some of them include:

* `os` and `sys`: These libraries provide functions for interacting with the operating system, such as file operations, directory handling, and system-related functionalities.
    
* `subprocess`: This library enables running external commands and managing subprocesses from within Python.
    
* `paramiko` and `fabric`: These libraries are used for SSH connectivity and remote command execution, which are often required in infrastructure automation tasks.
    
* `requests`: It is a popular library for making HTTP requests and interacting with web services.
    
* `docker` and `kubernetes`: These libraries provide APIs for managing Docker containers and Kubernetes clusters programmatically.
    

Remember to install any required libraries using `pip` before using them in your Python code.

### 💻Let's code

![](https://media.tenor.com/y2JXkY1pXkwAAAAM/cat-computer.gif )

1. Create a Dictionary in Python and write it to a JSON File.
    

```python
import json

# Create a dictionary
data = {
    'name': 'Swapnil Khairnar',
    'age': 23,
    'city': 'Bengaluru'
}

# Write the dictionary to a JSON file
with open('data.json', 'w') as file:
    json.dump(data, file)
```

In the above example, we first create a dictionary called `data` with some key-value pairs. Then, we use the `json.dump()` function to write the dictionary to a JSON file named `data.json`. The file is opened in write mode (`'w'`), and the `json.dump()` function serializes the dictionary and writes it to the file.

After running this code, you will have a JSON file named `data.json` containing the dictionary in JSON format.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686993195741/749a2734-a11a-424b-a511-809ef5ee5372.png )

2. Read a JSON file `services.json` kept in this folder and print the service names of every cloud service provider.
    

```python
output

aws : ec2
azure : VM
gcp : compute engine
```

here's an example of how to read a JSON file in Python and print the service names of every cloud service provider:

```python
import json

# Read the JSON file
with open("service.json", "r") as f:
    data = json.load(f)

# Extract the service names for each provider
for provider, services in data.items():
    print(f"{provider}: {services['service']}")
```

In this example, we first open the file `services.json` in read mode and use the `json.load()` function to load its contents into a Python object called `data`.

The `data` object is a dictionary where each key represents a cloud service provider, and the corresponding value is another dictionary containing information about their services. To extract the service name for each provider, we iterate over the key-value pairs in `data` using a for loop.

For each provider, we print the provider's name followed by the value associated with the key `"service"` in their corresponding dictionary. This should produce output that looks like this:

```python
aws: ec2
azure: VM
gcp: compute engine
```

3. Read YAML file using python, file `services.yaml` and read the contents to convert yaml to json

here's an example of how to read a YAML file in Python, and then convert it to JSON:

```python
import yaml
import json

# Read the YAML file
with open("services.yaml", "r") as f:
    data = yaml.safe_load(f)

# Convert YAML to JSON
json_data = json.dumps(data)

# Print the JSON data
print(json_data)
```

In this example, we first open the file `services.yaml` in read mode and use the [`yaml.safe`](http://yaml.safe)`_load()` function to load its contents into a Python object called `data`.

The `data` object is a dictionary where each key represents a cloud service provider, and the corresponding value is another dictionary containing information about their services.

To convert the `data` object to JSON format, we use the `json.dumps()` function, which converts a Python object to a JSON-formatted string.

Finally, we print the JSON data using the `print()` function. This should produce output that looks similar to the following:

```python
{
    "aws": {
        "service": "ec2",
        "description": "Elastic Compute Cloud"
    },
    "azure": {
        "service": "VM",
        "description": "Virtual Machines"
    },
    "gcp": {
        "service": "compute engine",
        "description": "Compute Engine"
    }
}
```

***Thanks for reading my article. Have a nice day.***

![No alt text provided for this image](https://media.licdn.com/dms/image/D4D12AQHNlk8ZIYUrAA/article-inline_image-shrink_1500_2232/0/1675886031853?e=1689811200&v=beta&t=lTPiTxCi1a0PbsEsySKh5fvp6gDIMlaAaq6Q9xtUKhQ )

For updates follow me on **LinkedIn**: [Swapnil Khairnar](https://www.linkedin.com/in/swapnilkhairnar78/)

---

Hashtags:

[#90daysofdevops](https://www.linkedin.com/feed/hashtag/90daysofdevops)  [#devops](https://www.linkedin.com/feed/hashtag/devops)  [#cloud](https://www.linkedin.com/feed/hashtag/cloud)  [#aws](https://www.linkedin.com/feed/hashtag/aws)  [#awscloud](https://www.linkedin.com/feed/hashtag/awscloud)  [#awscommunity](https://www.linkedin.com/feed/hashtag/awscommunity)  [#docker](https://www.linkedin.com/feed/hashtag/docker)  [#linux](https://www.linkedin.com/feed/hashtag/linux)  [#kubernetes](https://www.linkedin.com/feed/hashtag/kubernetes)  [#k8s](https://www.linkedin.com/feed/hashtag/k8s)  [#ansible](https://www.linkedin.com/feed/hashtag/ansible)  [#grafana](https://www.linkedin.com/feed/hashtag/grafana)  [#terraform](https://www.linkedin.com/feed/hashtag/terraform)  [#github](https://www.linkedin.com/feed/hashtag/github)  [#opensource](https://www.linkedin.com/feed/hashtag/opensource)  [#90daysofdevops](https://www.linkedin.com/feed/hashtag/90daysofdevops)  [#challenge](https://www.linkedin.com/feed/hashtag/challenge)  [#learningprogress](https://www.linkedin.com/feed/hashtag/learningprogress)  [#freelancer](https://www.linkedin.com/feed/hashtag/freelancer)  [#linkedin](https://www.linkedin.com/feed/hashtag/linkedin)  [#trainwithshubham](https://www.linkedin.com/feed/hashtag/trainwithshubham)  [#devopscommunity](https://www.linkedin.com/feed/hashtag/devopscommunity)  [#cloudproviders](https://www.linkedin.com/feed/hashtag/cloudproviders)  [#bash](https://www.linkedin.com/feed/hashtag/bash) [#bashshellscripting](https://www.linkedin.com/feed/hashtag/bashshellscripting) [#awkward](https://www.linkedin.com/feed/hashtag/awkward) [#shellscripting](https://www.linkedin.com/feed/hashtag/shellscripting)