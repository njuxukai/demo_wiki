# mm_trading_proxy_sub_thread

| server/client | topic                           | init时机 | 模式    |
| ------------- | ------------------------------- | -------- | ------- |
| client_       | MM_TOPIC_INIT                   | init     | pub/sub |
| client_       | MM_TOPIC_TRADING_COMMAND        | init     | pub/sub |
| client_       | MM_TOPIC_OUTSIDE_TRADING_RESULT | init     | pub/sub |

# mm_trading_proxy_pub_thread

| server/client | topic                              | init时机 | 模式    |
| ------------- | ---------------------------------- | -------- | ------- |
| server_       | MM_TOPIC_TRADING_PROXY_RAW_TRADING | init     | pub/sub |
|               |                                    |          |         |
|               |                                    |          |         |

