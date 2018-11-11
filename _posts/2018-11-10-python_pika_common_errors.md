---
layout: post
title: python pika common errors
description: python pika 13 common errors
category: blog
---

https://www.cloudamqp.com/blog/2018-01-19-part4-rabbitmq-13-common-errors.html

https://medium.com/@tonywangcn/building-a-more-practical-distributed-crawler-with-fabric-d3d7574bc9aa

celery rabbitmq redis fab

To launch remote command

AWS:
https://814008303944.signin.aws.amazon.com/console 
name is my domain account name
password is the numbers with six digits

Fabric 
http://www.bjhee.com/fabric.html
http://www.bjhee.com/

https://hackernoon.com/top-12-things-that-destroy-developer-productivity-2ddf0abc190

Notes:
http://www.wklken.me/

1) 
from fabric import task, Connection

@task
def staging(ctx):
    ctx.name = 'staging'
    ctx.user = 'ubuntu'
    ctx.host = '192.1.1.1'
    ctx.connect_kwargs.key_filename = os.environ['ENV_VAR_POINTS_TO_PRIVATE_KEY_PATH']

@task
def do_something_remote(ctx):
    with Connection(ctx.host, ctx.user, connect_kwargs=ctx.connect_kwargs) as conn:
        conn.sudo('supervisorctl status')

2) 
from fabric.api import *

env.hosts = ['host.name.com']
env.user = 'user'
env.key_filename = '/path/to/keyfile.pem'

def local_uname():
    local('uname -a')

def remote_uname():
    run('uname -a')
https://stackoverflow.com/questions/5327465/using-an-ssh-keyfile-with-fabric/9887656

https://www.ibm.com/developerworks/cn/linux/simplyfy-linux-deployment-with-fabric/index.html

https://www.abhishek-tiwari.com/amqp-rabbitmq-and-celery-a-visual-guide-for-dummies/

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"

