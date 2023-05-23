# Azure.Storage.Blobs.Manager

![Build](https://img.shields.io/github/actions/workflow/status/Matozap/Azure.Storage.Blobs.Manager/build.yml?style=for-the-badge&logo=github&color=0D7EBF)
![Commits](https://img.shields.io/github/last-commit/Matozap/Azure.Storage.Blobs.Manager?style=for-the-badge&logo=github&color=0D7EBF)
![Package](https://img.shields.io/nuget/dt/Azure.Storage.Blobs.Manager?style=for-the-badge&logo=nuget&color=0D7EBF)


Azure.Storage.Blobs.Manager is an Injectable abstraction to download, upload, move, map, read and delete blobs from Azure.


It simplifies storage usage by allowing developers to inject it into the application and use it anywhere
without having to worry about the azure client. 

------------------------------

### Usage

#### Injection

Just inject and use the ICache interface to store or obtain values from the cache like the example below:

```csharp

public class SomeService
{
    private readonly IBlobStorageManager _storageManager;

    public SomeService(IBlobStorageManager storageManager)
    {
        _storageManager = storageManager;
    }    
}

```


### Configuration

#### Startup/program 

Just add below lines to have the IBlobStorageManager registered in the service collection and ready to use anywhere.

```csharp
services.AddAzureBlobStorage(options =>
{
    options.WithEndpoint("<storage endpoint>");
});
```

###

## Contributing

It is simple, as all things should be:

1. Clone it
2. Improve it
3. Make pull request

## Credits

- Initial development by [Slukad](https://github.com/Slukad)
