# Redis & Sentinel - high availability replica example

> Redis high availability replica docker setup with 3 nodes: master (172.20.0.2), slave1 (172.20.0.3), slave2 (172.20.0.4)

## 1 - How to setup
> docker-compose up -d

## 2 - How to check current master in Redis Sentinel
> redis-cli -p 26379 SENTINEL masters

## 3 - How to test
> **1** - Start redis replica with docker-compose command

> **2** - Shut down master (redis_m container) & wait 10 seconds till Sentinel promote one of the slaves into new master
