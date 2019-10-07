# SHCommonSDK-Framework

 SHCommonSDK-Framework

## All method description

- deviveID: Get the device identify
- deviceName: Get the device name
- platformName: Get the ios version
- bundleResourceByName: Get the bundle by name
- requestSynchronous: Send a synchronous request to server
- requestAsynchronous: Send a asynchronous request to server

## How to use

First create SHCommonSDK object

```objc
SHCommonSDK *commonSDK = [[SHCommonSDK alloc] init];
```

- Get device identify

```objc
    NSString *deviceID = [commonSDK deviceID];
```

- Get divice name

```objc
    NSString *deviceID = [commonSDK deviceName];
```

- Get platform name

```objc
    NSString *platformName = [commonSDK platformName];
```

- Get bundel by name

```objc
    NSString *phoneName = [commonSDK bundleResourceByName:@"The name];
```
