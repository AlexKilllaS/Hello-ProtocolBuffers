# Hello-ProtocolBuffers
alex huangfu
## 1. Background
[Protocol Buffers](https://protobuf.dev/) are language-neutral, platform-neutral extensible mechanisms for serializing structured data.

_advantages_:
1. Compact data storage
2. Fast parsing
3. Availability in many programming languages
4. Optimized functionality through automatically-generated classes

Use Java Protocol Buffers To use protobuf in Java, first obtain the protocol compiler and use it to generate Java code for your .proto files:

`$ protoc --java_out=${OUTPUT_DIR} path/to/your/proto/file`
Include the generated Java files in your project and add a dependency on the protobuf Java runtime.

### Maven
If you are using Maven, use the following:
```xml
<dependency>
  <groupId>com.google.protobuf</groupId>
  <artifactId>protobuf-java</artifactId>
  <version>3.25.0</version>
</dependency>
```
Make sure the version number of the runtime matches (or is newer than) the version number of the protoc.

If you want to use features like protobuf JsonFormat, add a dependency on the protobuf-java-util package:

```xml
<dependency>
  <groupId>com.google.protobuf</groupId>
  <artifactId>protobuf-java-util</artifactId>
  <version>3.25.0</version>
</dependency>
```

### Use Java Protocol Buffers on Android
For Android users, it's recommended to use protobuf Java Lite runtime because of its smaller code size. Java Lite runtime also works better with Proguard because it doesn't rely on Java reflection and is optimized to allow as much code stripping as possible. You can follow these instructions to use Java Lite runtime.

## 2. Background