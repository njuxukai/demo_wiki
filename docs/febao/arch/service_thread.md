# event_service_thread

async_log_thread

| 接口                          | 场景                                       |      |
| ----------------------------- | ------------------------------------------ | ---- |
| register_start_in_thread_func | 1 例如lev2行情网关中，轮询获取行情         |      |
| register_do_task_function     | mm_trading_biz_thread 读取流               |      |
| set_name                      |                                            |      |
| register_timer_function       | mm_local_table_storage_manager刷新回数据库 |      |
| register_stop_in_thread_func  |                                            |      |
| post(functor)                 |                                            |      |
|                               |                                            |      |
|                               |                                            |      |
|                               |                                            |      |



# io_service_thread

| 接口                          | 场景                                       |      |
| ----------------------------- | ------------------------------------------ | ---- |
| register_start_in_thread_func | 1 例如lev2行情网关中，轮询获取行情         |      |
| register_do_task_function     | mm_trading_biz_thread 读取流               |      |
| set_name                      |                                            |      |
| register_timer_function       | mm_local_table_storage_manager刷新回数据库 |      |
| register_stop_in_thread_func  |                                            |      |
| post(functor)                 |                                            |      |
|                               |                                            |      |
|                               |                                            |      |
|                               |                                            |      |

