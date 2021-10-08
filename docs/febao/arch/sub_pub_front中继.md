![image-20210520145642377](sub_pub_front中继.assets/image-20210520145642377-1621493809952.png)

on_service_req

![image-20210520145908832](sub_pub_front中继.assets/image-20210520145908832-1621493950852.png)

在server处得到新的request, 将message_node,  decoder_(copy from decoder_)发往client





![image-20210520151218409](sub_pub_front中继.assets/image-20210520151218409-1621494742140.png)

在client处得到response,client将context带出，供回调使用



context 是可以灵活定义的， request的时候存入，这里注意的是encoder_ 保存reqeust_id_的时机 ，后续得到的rsp 使用seq_no字段将原reqeust_id返回，在session中处理时，可以找到相应的context

