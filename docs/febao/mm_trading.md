# mm_trading_sub_thread

| server/client | topic                                | init时机   | 角色    |
| ------------- | ------------------------------------ | ---------- | ------- |
| client        | MM_TOPIC_INIT                        | init       | pub/sub |
| client        | MM_TOPIC_TRADING_RAW_TRADING(s)      | start_work | pub/sub |
| client        | MM_TOPIC_TRADING_RAW_QUERY(s)        | start_work | req/rsp |
| client        | MM_TOPIC_STRATEGY_TRADING_COMMAND(s) | start_work | pub/sub |
| server        | MM_TOPIC_TRADING_SERVICE             | start_work | req/rsp |



# mm_trading_pub_thread

| server/client | topic                    | init时机 | 角色    |
| ------------- | ------------------------ | -------- | ------- |
| inner_server_ | MM_TOPIC_TRADING_RESULT  | init     | pub/sub |
| upper_server_ | MM_TOPIC_TRADING_COMMAND | init     | pub/sub |
| upper_server_ | MM_TOPIC_TRADING_OUTSIDE | int      | pub/sub |



# mm_trading_biz_thread



# 源代码组织

| 目录          |      |      |
| ------------- | ---- | ---- |
| biz           |      |      |
| common        |      |      |
| main          |      |      |
| msg_handler   |      |      |
| rule          |      |      |
| rule_group    |      |      |
| timer_handler |      |      |

