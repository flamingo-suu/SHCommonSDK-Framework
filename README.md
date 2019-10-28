# SHCommonSDK-Framework

 SHCommonSDK-Framework

## Implementation

In your podfile add the following command

```ruby
pod 'SHCommonSDK'
```

## All method description

- `getDeviveUID`: Get the device identify
- `getDeviceName`: Get the device name
- `getPlatformName`: Get the ios version
- `getBundleResourceByName`: Get the bundle by name
- `convertNSStringToNSData`: Convert a NSString to NSData
- `convertNSDataToNSString`: Convert a NSData to NSString
- `convertNSStringToNSDictionary`: Convert NSString (JSON) to NSDictionary
- `convertNSDictionaryToNSString`: Convert NSDictionary to NSString(JSON)
- `requestSynchronous`: Send a synchronous request to server to get data
- `requestAsynchronous`: Send an asynchronous request to server to get data

## How to use

- **Get unique device identify**

```objc
    NSString *deviceUID = [SHCommonSDK getDeviceUID];
```

- **Get divice name**

```objc
    NSString *deviceName = [SHCommonSDK getDeviceName];
```

- **Get platform name**

```objc
    NSString *platformName = [SHCommonSDK getPlatformName];
```

- **Get bundle by name**

```objc
    NSBundle *bundle = [SHCommonSDK getBundleResourceByName:@"Main"];
```

## All other method need to create SHCommonSDK object

```objc
    SHCommonSDK *commonSDK = [[SHCommonSDK alloc] init];
```

- **Convert NSString to NSData**

```objc
    NSData *data = [commonSDK convertNSStringToNSData:@"String data"];
```

- **Convert NSData to NSString**

```objc
    NSString *str = [commonSDK convertNSDataToNSString:data];
```

- **Convert NSString to NSDictionary**

```objc
    NSDictionary *ditionary = [commonSDK convertNSStringToNSDictionary:@"{\"ID\":{\"Content\":268,\"type\":\"text\"}"];
```

- **Convert NSDictionary to NSString**

```objc
    NSString *str = [commonSDK convertNSDictionaryToNSString:ditionary];
```

- **Send synchronous request to server url**

```objc
    NSDictionary<NSString *,NSString *> *header = [commonSDK convertNSStringToNSDictionary:@"{\"ID\":{\"Content\":268,\"type\":\"text\"}"];
    NSData *params = [commonSDK convertNSStringToNSDictionary:@"DATA"];
    NSData *data = [commonSDK requestSynchronous:@"http://url"
        withMethod:APIMethodGet
        withHeader:header
        withParams:params];
```

- **Send asynchronous request to server url**

```objc
        NSDictionary<NSString *,NSString *> *header = [commonSDK convertNSStringToNSDictionary:@"{\"ID\":{\"Content\":268,\"type\":\"text\"}"];
    NSData *params = [commonSDK convertNSStringToNSDictionary:@"DATA"];
    [commonSDK requestAsynchronous:@"https://url"
        withMethod:APIMethodGet
        withHeader:header
        withParams:params
        completeHandle:callback];
    // callback example
    // - (void (^)(NSURLResponse *, NSData *, NSError *))callback {
    //      return ^(NSURLResponse *urlResponse, NSData *data, NSError *error) {
    //
    //};
}
```
