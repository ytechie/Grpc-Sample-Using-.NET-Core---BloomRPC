# Grpc Sample Using .NET Core + BloomRPC
 
 A working .NET Core sample that publishes a simple gRPC service that can be consumed by the [BloomRPC Client](https://github.com/uw-labs/bloomrpc).

 Simply run the project, and configure BloomRPC as show below.

 ![Bloom RPC Configuration](bloomrpc-screenshot.png)

 ### Background

 This is basically a stock RPC sample, but with the following addition:

 ```
	webBuilder.ConfigureKestrel(options =>
    {
        // This endpoint will use HTTP/2 and HTTPS on port 5001.
        options.Listen(IPAddress.Any, 5001, listenOptions =>
        {
            listenOptions.Protocols = HttpProtocols.Http2;
        });
    });
 ```