# Nexmo APIs code snippets for .NET using CSharp

<img src="https://developer.nexmo.com/assets/images/Vonage_Nexmo.svg" height="48px" alt="Nexmo is now known as Vonage" />

The purpose of the code snippets project is to provide simple examples focused on one goal. For example, sending an SMS, handling an incoming SMS webhook or making a Text to Speech call.

## Setup

These code examples are meant to be used in the manner described on [Nexmo's Developer Portal](https://developer.nexmo.com) for example [Sending an SMS](https://developer.nexmo.com/messaging/sms/code-snippets/send-an-sms/dotnet). This repo is structured in such a way as to support internal testing. Developers are free to use these snippets as a reference - but they may require some changes to get them to work inside your application. 

If you'd like to run this application yourself you'll need to configure your Nexmo Credentials

### Configure your Nexmo Credentials for SMS, Management APIs, Verify, Numbers Insight

To use this sample you will first need a [Nexmo account](https://dashboard.nexmo.com/sign-up). Once you have your own API credentials, you'll need to set them in the Client Constructors - for most of the API's you can set them in [BasicAuth.cs](https://github.com/Nexmo/nexmo-dotnet-code-snippets/blob/master/NexmoDotnetCodeSnippets/Authentication/BasicAuth.cs).

### Configure your Nexmo Credentials for Voice:

For Voice API usage you will need to set the Application ID and Private Key as well in the [FullAuth.cs](https://github.com/Nexmo/nexmo-dotnet-code-snippets/blob/master/NexmoDotnetCodeSnippets/Authentication/FullAuth.cs) file

### Configuring your credentials and settings with appsettings.json

Alternatively, provide the nexmo URLs, API key, secret, and application credentials (for JWT) in ```appsettings.json```:

```json
{
  "appSettings": {
    "Nexmo.UserAgent": "myApp/1.0",
    "Nexmo.Url.Rest": "https://rest.nexmo.com",
    "Nexmo.Url.Api": "https://api.nexmo.com",
    "Nexmo.api_key": "NEXMO-API-KEY",
    "Nexmo.api_secret": "NEXMO-API-SECRET",
    "Nexmo.Application.Id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
    "Nexmo.Application.Key": "NEXMO_APPLICATION_PRIVATE_KEY"
  }
}
```

For some of the examples, you will need to [buy a number](https://dashboard.nexmo.com/buy-numbers).

### TLS Upgrade

Nexmo permanently disabled support of legacy TLSv1 and TLSv1.1 protocols. Vulnerabilities within these TLS versions are serious and, left unaddressed, put organizations at risk of being breached. The only supported encryption protocol for HTTPS connections is now TLSv1.2. All API requests and all web requests to the Nexmo Dashboard using legacy TLS protocols will be rejected.

In case you are still using a legacy TLS protocol, make sure to force your app to TLSv1.2 by adding this line of code :

```csharp
System.Net.ServicePointManager.SecurityProtocol =  System.Net.SecurityProtocolType.Tls12;
```

## Request an Example

Please [raise an issue](https://github.com/nexmo-community/nexmo-dotnet-quickstart/issues) to request an example that isn't present within the code snippets. Pull requests will be gratefully received.

## License

This code is licensed under the [MIT](https://github.com/nexmo-community/nexmo-java-quickstart/blob/master/LICENSE.txt) license.
