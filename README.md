# Azure Function with Custom Image

Custom image for an Azure Functions application.

## Local development

Start the storage emulator:

```sh
azurite-blob -l azurite
```

Create the settings file:

```sh
cp local.settings.Development.json local.settings.json
```

Install and start the app:

```sh
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

func start
```

## Docker



### Reference

[Create a function on Linux using a custom container](https://docs.microsoft.com/en-us/azure/azure-functions/functions-create-function-linux-custom-image?tabs=bash%2Cportal&pivots=programming-language-python)