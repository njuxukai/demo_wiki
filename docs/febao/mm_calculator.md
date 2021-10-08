## mm_calculator_sub_thread

​	

| client/server | topic                           | init时机   | mode            |
| ------------- | ------------------------------- | ---------- | --------------- |
| client        | MM_TOPIC_INIT                   | init       | pub/sub         |
| server        | MM_TOPIC_CALCULATOR_SERVICE     | init       | req/rsp         |
| client        | MM_TOPIC_MD_PROXY_RAW_MD(s)     | start_work | req/rsp,pub/sub |
| client        | MM_TOPIC_TRADING_PROXY_QUERY(s) | start_work | req/rsp         |
| client        | MM_TOPIC_PRICING_DERIVED_MD     | start_work | req/rsp.pub/sub |
| client        | MM_TOPIC_TRADING_RESULT         | start_work | pub/sub         |



## mm_calculator_pub_thread

| client/server | topic                       | init时机 |      |
| ------------- | --------------------------- | -------- | ---- |
| server        | MM_TOPIC_CALCULATOR_RESULT  | init     | pub  |
| server        | MM_TOPIC_CALCULATOR_TRADING | init     | pub  |

