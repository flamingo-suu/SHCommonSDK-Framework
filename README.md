# SHCommonSDK-Framework

 SHCommonSDK-Framework

## Implementation

pod 'SHCommonSDK', '~> 0.0.2'

## All method description

- deviveID: Get the device identify
- deviceName: Get the device name
- platformName: Get the ios version
- bundleResourceByName: Get the bundle by name
- requestSynchronous: Send a synchronous request to server
- requestAsynchronous: Send a asynchronous request to server

## How to use

> **First create SHCommonSDK object**

```objc
SHCommonSDK *commonSDK = [[SHCommonSDK alloc] init];
```

- **Get device identify**

```objc
    NSString *deviceID = [commonSDK deviceID];
```

- **Get divice name**

```objc
    NSString *deviceID = [commonSDK deviceName];
```

- **Get platform name**

```objc
    NSString *platformName = [commonSDK platformName];
```

- **Get bundel by name**

```objc
    NSBundle *bundle = [commonSDK bundleResourceByName:@"The name];
```

- **Request from server using synchronous**

```objc
    NSBundle *bundle = [commonSDK bundleResourceByName:@"The name];
```

- **Convert NSString to NSData**

```objc
    NSData *data = [convertNSStringToNSData:@"String data"];
```

- Convert NSData to NSString

```objc
    NSString *str = [convertNSDataToNSString:data];
```

- **Convert NSString to NSDictionary**

```objc
    NSDictionary *ditionary = convertNSStringToNSDictionary:@"{"id":"123","name":"SHCommon"}";
```

- **Convert NSDictionary to NSString**

```objc
    NSString *str = convertNSDictionaryToNSString:ditionary;
```

- **Send asynchronous request to server url**

```objc
    requestAsynchronous:(NSString *)url
                 withMethod:(APIMethod)method
                 withHeader:(NSDictionary<NSString *, NSString *> *)header
                 withParams:(NSData *)params
             completeHandle:(void (^)(NSURLResponse *urlResponse, NSData *data, NSError *error))callback ;
```

- **Send synchronous request to server url**

```objc
    (NSData *)requestSynchronous:(NSString *)url
                    withMethod:(APIMethod)method
                    withHeader:(NSDictionary<NSString *, NSString *> *)header
                    withParams:(NSData *)params;
```
