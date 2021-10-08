# mm_front_sub_thread

| server/client | topic                        | init时机   | 模式    |
| ------------- | ---------------------------- | ---------- | ------- |
| client_       | MM_TOPIC_INIT                | init       | pub/sub |
| client_       | MM_TOPIC_MD_PROXY_RAW_MD(s)  | start_work | pub/sub |
| client_       | MM_TOPIC_STRATEGY_SERVICE(s) | start_work | pub/sub |
| client_       | MM_TOPIC_TRADING_RESULT      | start_work | pub/sub |
| client_       | MM_TOPIC_PRICING_DERIVED_MD  | start_work | pub/sub |
| client_       | MM_TOPIC_CALCULATE_RESULT    | start_work | pub/sub |

| 函数                              |                                                              |
| --------------------------------- | ------------------------------------------------------------ |
| init()                            | j                                                            |
| on_init_pub(const biz_decoder* d) | （MM_TOPIC_INIT）set_sub_scribe_callback的回调函数，1 调用pub->on_data() 2 如果是MSG）END_INIT 注册tpoic |
| on_pub                            | (其他topic)的set_sub_scribe_callback回调函数 1CFFEX_TAG  2 pub->on_data() |



# mm_front_pub_thread

| server/client | topic                  | init时机 | 模式    |
| ------------- | ---------------------- | -------- | ------- |
| server_       | MM_TOPIC_FRONT_SUMMARY | init     | pub/sub |
|               |                        |          |         |
|               |                        |          |         |

| 函数                          |                                                              |
| ----------------------------- | ------------------------------------------------------------ |
| on_data(const biz_decoder* d) | 将数据封装为pub_event，放入队列                              |
| do_publish(void* e)           | pub_event的回调函数，在server_（MM_TPOIC_FRONT_SUMMARY）发布 |
|                               |                                                              |



# mm_front_service_thread

| server/client | topic                        | init时机 | 模式    |
| ------------- | ---------------------------- | -------- | ------- |
| server_       | MM_TOPIC_FRONT_SERVICE       | init     | req/rsp |
| client_       | MM_TOPIC_INIT_SERVICE        | init     | req/rsp |
| client_       | MM_TOPIC_TRADING_SERVICE     | init     | req/rsp |
| client_       | MM_TOPIC_CALCULATE_SERVICE   | init     | req/rsp |
| client_       | MM_TOPIC_STRATEGY_SERVICE(s) | init     | req/rsp |

| 函数           |                                                           |
| -------------- | --------------------------------------------------------- |
| init           |                                                           |
| on_service_req | server_(MM_TOPIC_FRONT_SERVICE)的request_callback注册回调 |
|                |                                                           |
|                |                                                           |
|                |                                                           |

