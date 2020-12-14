# Project1 StandaloneKV

> https://github.com/tidb-incubator/tinykv/blob/course/doc/project1-StandaloneKV.md

## gRPC

> https://grpc.io/docs/what-is-grpc/introduction/

+ **RPC**:
  + https://www.zhihu.com/question/25536695/answer/221638079
  + 本地调用远程接口
  + 三个机制：CallID\序列化和反序列化\网络传输（大部分:TCP,gRPC:HTTP2）

+ **protocol buffer**
  + 一种轻便高效的结构化数据存储格式，可以用于结构化数据序列化，很适合做数据存储或 RPC 数据交换格式。它可用于通讯协议、数据存储等领域的语言无关、平台无关、可扩展的序列化结构数据格式。



Txn := s.engines.Kv.NewTransaction(bool) //新建transaction

新建storageReader结构用于返回

这个bool代表update，目前不知道用处

## Go

/kv/storage/modify.go

type Modify struct {

  Data interface{}

}

+ interface{} 类型，空接口 for all type

