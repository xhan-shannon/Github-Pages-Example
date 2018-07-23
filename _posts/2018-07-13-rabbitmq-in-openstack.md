---
layout: post
title: rabbitmq in openstack
description: To learn and make clear how rabbitmq works in openstack
category: blog
---

## rabbitmq in openstack

## check connection using Linux command 

## check connection using rabbitmqctl
1. at server side , the central UI starts
$ sudo rabbitmqctl list_connections 
[sudo] password for cuda: 
Listing connections
cqa	127.0.0.1	58168	running
cqa	127.0.0.1	58170	running
 
2. check the exchanges
$ sudo rabbitmqctl list_exchanges -p cqa_engine
Listing exchanges
rpc_service	direct
controller	direct
monitor	        fanout
taskengine	direct

3. check the queues
$ sudo rabbitmqctl list_queues -p cqa_engine
Listing queues
amq.gen-0FObo_TxLfaNPrjZfMvZ1g	0
amq.gen-iJydUza86-7cqglTWa55Kw	0
rpc_queue	0
cmdaction_queue	0
report_queue

4. check the bindings
$ sudo rabbitmqctl list_bindings -p cqa_engine
Listing bindings
	exchange	amq.gen-0FObo_TxLfaNPrjZfMvZ1g	queue	amq.gen-0FObo_TxLfaNPrjZfMvZ1g	[]
	exchange	amq.gen-iJydUza86-7cqglTWa55Kw	queue	amq.gen-iJydUza86-7cqglTWa55Kw	[]
	exchange	cmdaction_queue	queue	cmdaction_queue	[]
	exchange	report_queue	queue	report_queue	[]
	exchange	rpc_queue	queue	rpc_queue	[]
controller	exchange	cmdaction_queue	queue	cmd_routing_key.131017457602844	[]
monitor	exchange	amq.gen-iJydUza86-7cqglTWa55Kw	queue	amq.gen-iJydUza86-7cqglTWa55Kw	[]
rpc_service	exchange	amq.gen-0FObo_TxLfaNPrjZfMvZ1g	queue	amq.gen-0FObo_TxLfaNPrjZfMvZ1g	[]
rpc_service	exchange	rpc_queue	queue	rpc_queue	[]
taskengine	exchange	report_queue	queue	report_routing_key	[]



[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
