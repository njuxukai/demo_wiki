# mm_strategy_sub_thread

| server/client | topic                       | init时机   | 模式            |
| ------------- | --------------------------- | ---------- | --------------- |
| client_       | MM_TOPIC_INIT               | init       | pub/sub         |
| client_       | MM_TOPIC_MD_PROXY_RAW_MD(s) | start_work | pub/sub,req/rsp |
| client_       | MM_TOPIC_PRICING_DERIVED    | start_work | pub/sub,req/rsp |
| client_       | MM_TOPIC_TRADING_RESULT     | start_work | pub/sub         |
| client_       | MM_TOPIC_CALCULATE_RESULT   | start_work | pub/sub         |
|               |                             |            |                 |



# mm_strategy_pub_thread

| server/client | topic                             | init时机 | 模式    |
| ------------- | --------------------------------- | -------- | ------- |
| server_       | MM_TOPIC_STRATEGY_TRADING_COMMAND | init     | pub/sub |
| server_       | MM_TOPIC_STRATEGY_SERVICE         | init     | req/rsp |
| server_       | MM_TOPIC_STRATEGY_SYNC_DB         | init     | pub/sub |

