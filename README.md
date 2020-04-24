# Azure Function with Custom Image

### Running it

```sh
python3 -m venv .venv
source .venv/bin/activate
func start --build
```

### Infrastructure

```sh
az storage account create -n <name> -g <group> -l <location> --sku Standard_LRS
az storage account show-connection-string -g <group> -n <name>
```

### Building from scratch

```
sudo apt-get install python3-venv
python3 -m venv .venv
source .venv/bin/activate
func init . --worker-runtime python --docker
func new --name ProducerFunction --template "TimerTrigger"
func start --build
```

### Reference

[Create a function on Linux using a custom container](https://docs.microsoft.com/en-us/azure/azure-functions/functions-create-function-linux-custom-image?tabs=bash%2Cportal&pivots=programming-language-python)