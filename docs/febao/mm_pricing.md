# mm_pricing_sub_thread

| server/client | topic                       | init时机   | 模式            |
| ------------- | --------------------------- | ---------- | --------------- |
| client_       | MM_TOPIC_INIT               | init       | pub/sub         |
| client_       | MM_TOPIC_MD_PROXY_RAW_MD(s) | start_work | pub/sub,req/rsp |
|               |                             |            |                 |



# mm_pricing_pub_thread

| server/client | topic                       | init时机 | 模式    |
| ------------- | --------------------------- | -------- | ------- |
| server_       | MM_TOPIC_PRICING_DERIVED_MD | init     | pub/sub |
|               |                             |          |         |
|               |                             |          |         |

# 

