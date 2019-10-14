数据包大小设置
==
默认数据包大小为8M，即服务的请求和返回值序列化后默认不超过8M，要不然数据接收方会丢弃此数据。
数据较大，建议开启调用压缩，如果压缩后数据还大，可以进行自定义数据包配置。
>说明：下面示例中采用  **`<beans/>`** 标签 表示JOYRPC中的schema。

- 1. 如果请求值数据较大，则服务提供者进行配置。

- 2. 如果是返回值数据较大，则服务调用者进行配置。

  ```xml
  <beans>

   <!-- 全局参数：默认是8388608=8*1024*1024 -->
  <joyrpc:parameter key="payload" value="16777216" /> 
  </beans>
  ```