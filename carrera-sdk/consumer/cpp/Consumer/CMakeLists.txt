cmake_minimum_required(VERSION 3.12)
project(Consumer)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
include_directories(thirdparty/carrera)
include_directories(thirdparty/thrift)
include_directories(thirdparty/thrift/async)
include_directories(thirdparty/thrift/c_glib)
include_directories(thirdparty/thrift/c_glib/processor)
include_directories(thirdparty/thrift/c_glib/protocol)
include_directories(thirdparty/thrift/c_glib/server)
include_directories(thirdparty/thrift/c_glib/transport)
include_directories(thirdparty/thrift/concurrency)
include_directories(thirdparty/thrift/processor)
include_directories(thirdparty/thrift/protocol)
include_directories(thirdparty/thrift/qt)
include_directories(thirdparty/thrift/server)
include_directories(thirdparty/thrift/transport)

add_executable(Consumer
        thirdparty/carrera/CarreraClient.h
        thirdparty/carrera/consumerProxy_constants.h
        thirdparty/carrera/consumerProxy_types.h
        thirdparty/carrera/ConsumerService.h
        thirdparty/carrera/mq_logger.h
        thirdparty/carrera/SimpleCarreraClient.h
        thirdparty/thrift/async/TAsyncBufferProcessor.h
        thirdparty/thrift/async/TAsyncChannel.h
        thirdparty/thrift/async/TAsyncDispatchProcessor.h
        thirdparty/thrift/async/TAsyncProcessor.h
        thirdparty/thrift/async/TAsyncProtocolProcessor.h
        thirdparty/thrift/async/TEvhttpClientChannel.h
        thirdparty/thrift/async/TEvhttpServer.h
        thirdparty/thrift/c_glib/processor/thrift_dispatch_processor.h
        thirdparty/thrift/c_glib/processor/thrift_processor.h
        thirdparty/thrift/c_glib/protocol/thrift_binary_protocol.h
        thirdparty/thrift/c_glib/protocol/thrift_binary_protocol_factory.h
        thirdparty/thrift/c_glib/protocol/thrift_protocol.h
        thirdparty/thrift/c_glib/protocol/thrift_protocol_factory.h
        thirdparty/thrift/c_glib/server/thrift_server.h
        thirdparty/thrift/c_glib/server/thrift_simple_server.h
        thirdparty/thrift/c_glib/transport/thrift_buffered_transport.h
        thirdparty/thrift/c_glib/transport/thrift_buffered_transport_factory.h
        thirdparty/thrift/c_glib/transport/thrift_framed_transport.h
        thirdparty/thrift/c_glib/transport/thrift_framed_transport_factory.h
        thirdparty/thrift/c_glib/transport/thrift_memory_buffer.h
        thirdparty/thrift/c_glib/transport/thrift_server_socket.h
        thirdparty/thrift/c_glib/transport/thrift_server_transport.h
        thirdparty/thrift/c_glib/transport/thrift_socket.h
        thirdparty/thrift/c_glib/transport/thrift_transport.h
        thirdparty/thrift/c_glib/transport/thrift_transport_factory.h
        thirdparty/thrift/c_glib/config.h
        thirdparty/thrift/c_glib/thrift.h
        thirdparty/thrift/c_glib/thrift_application_exception.h
        thirdparty/thrift/c_glib/thrift_struct.h
        thirdparty/thrift/concurrency/BoostThreadFactory.h
        thirdparty/thrift/concurrency/Exception.h
        thirdparty/thrift/concurrency/FunctionRunner.h
        thirdparty/thrift/concurrency/Monitor.h
        thirdparty/thrift/concurrency/Mutex.h
        thirdparty/thrift/concurrency/PlatformThreadFactory.h
        thirdparty/thrift/concurrency/PosixThreadFactory.h
        thirdparty/thrift/concurrency/StdMonitor.cpp
        thirdparty/thrift/concurrency/StdMutex.cpp
        thirdparty/thrift/concurrency/StdThreadFactory.cpp
        thirdparty/thrift/concurrency/StdThreadFactory.h
        thirdparty/thrift/concurrency/Thread.h
        thirdparty/thrift/concurrency/ThreadManager.h
        thirdparty/thrift/concurrency/TimerManager.h
        thirdparty/thrift/concurrency/Util.h
        thirdparty/thrift/processor/PeekProcessor.h
        thirdparty/thrift/processor/StatsProcessor.h
        thirdparty/thrift/processor/TMultiplexedProcessor.h
        thirdparty/thrift/protocol/TBase64Utils.h
        thirdparty/thrift/protocol/TBinaryProtocol.h
        thirdparty/thrift/protocol/TBinaryProtocol.tcc
        thirdparty/thrift/protocol/TCompactProtocol.h
        thirdparty/thrift/protocol/TCompactProtocol.tcc
        thirdparty/thrift/protocol/TDebugProtocol.h
        thirdparty/thrift/protocol/TDenseProtocol.h
        thirdparty/thrift/protocol/TJSONProtocol.h
        thirdparty/thrift/protocol/TMultiplexedProtocol.h
        thirdparty/thrift/protocol/TProtocol.h
        thirdparty/thrift/protocol/TProtocolDecorator.h
        thirdparty/thrift/protocol/TProtocolException.h
        thirdparty/thrift/protocol/TProtocolTap.h
        thirdparty/thrift/protocol/TVirtualProtocol.h
        thirdparty/thrift/qt/TQIODeviceTransport.h
        thirdparty/thrift/qt/TQTcpServer.h
        thirdparty/thrift/server/TNonblockingServer.h
        thirdparty/thrift/server/TServer.h
        thirdparty/thrift/server/TSimpleServer.h
        thirdparty/thrift/server/TThreadedServer.h
        thirdparty/thrift/server/TThreadPoolServer.h
        thirdparty/thrift/transport/PlatformSocket.h
        thirdparty/thrift/transport/TBufferTransports.h
        thirdparty/thrift/transport/TFDTransport.h
        thirdparty/thrift/transport/TFileTransport.h
        thirdparty/thrift/transport/THttpClient.h
        thirdparty/thrift/transport/THttpServer.h
        thirdparty/thrift/transport/THttpTransport.h
        thirdparty/thrift/transport/TPipe.h
        thirdparty/thrift/transport/TPipeServer.h
        thirdparty/thrift/transport/TServerSocket.h
        thirdparty/thrift/transport/TServerTransport.h
        thirdparty/thrift/transport/TShortReadTransport.h
        thirdparty/thrift/transport/TSimpleFileTransport.h
        thirdparty/thrift/transport/TSocket.h
        thirdparty/thrift/transport/TSocketPool.h
        thirdparty/thrift/transport/TSSLServerSocket.h
        thirdparty/thrift/transport/TSSLSocket.h
        thirdparty/thrift/transport/TTransport.h
        thirdparty/thrift/transport/TTransportException.h
        thirdparty/thrift/transport/TTransportUtils.h
        thirdparty/thrift/transport/TVirtualTransport.h
        thirdparty/thrift/transport/TZlibTransport.h
        thirdparty/thrift/config.h
        thirdparty/thrift/cxxfunctional.h
        thirdparty/thrift/TApplicationException.h
        thirdparty/thrift/TDispatchProcessor.h
        thirdparty/thrift/thrift-config.h
        thirdparty/thrift/Thrift.h
        thirdparty/thrift/TLogging.h
        thirdparty/thrift/TProcessor.h
        thirdparty/thrift/TReflectionLocal.h
        thirdparty/thrift/TToString.h
        CarreraConsumer.cpp
        CarreraConsumer.h
        CarreraClientExample.cpp
        consumerProxy_constants.cpp
        consumerProxy_constants.h
        consumerProxy_types.cpp
        consumerProxy_types.h
        ConsumerService.cpp
        ConsumerService.h
        mq_logger.cpp
        mq_logger.h
        SimpleCarreraClient.cpp
        SimpleCarreraClient.h CarreraConfig.h CarreraDefine.h)
