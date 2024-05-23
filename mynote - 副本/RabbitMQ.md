<!--
 * @Author: kekexili1230 457738564@qq.com
 * @Date: 2024-01-20 16:35:30
 * @LastEditors: kekexili1230 457738564@qq.com
 * @LastEditTime: 2024-01-20 16:45:52
 * @FilePath: /mynote/RabbitMQ.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# RabbitMQ 

## AMQP（advance message queueing protocol）高级消息队列协议

是一个网络协议，应用层协议的开发标准。基于此协议的客户端和中间件可传递消息，并不受客户端和中间件的限制。

## RabbitMQ的基本概念

- 生产者：创建消息的一方

- 消费者：接受消息的一方

- Broker：消息中间件的服务节点

- virtual host：类似于租户和命名空间的概念

- Connection

- Channel

- exchange

    - direct

    - topic

    - fanout

- Queue

- Binding

## RabbitMQ的工作模式

- 简单模式

- work queue

- 发布、订阅

- routing路由

- topics