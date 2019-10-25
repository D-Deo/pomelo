# pomelo

## 添加 rpc 属性支持

_rpc 属性的作用，可以使服务器不会自动启动服务，需要的时候会通过远程模式访问（非ssh，tcp直连）_

**举例**
像案例所示的方式添加rpc参数，该user服务器不会以服务模式启动，只会在远程调用过程中直接搜索目标服务器
好处是未了避开 ssh 启动的方式，分布式部署更容易
```json
{
    "user": [
        {"id": "user-server", "host": "127.0.0.1", "rpc":true, "port": 32001, "needed": true, "wsdebug": false }
    ],
}
```