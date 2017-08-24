kafkaClient
===========

Describe:   kafka simple producer/consumer  

From:     frank.zhao kafka-client  

Dependency:     kafka version: 0.10.0.1, jdk1.8  

---

### Get Start:  

    com.simple.kafka.consumer.KafkaConsumer      消费者
        sample:
            'new KafkaConsumer<String, String>(props).build().consumer("test", 3 , s -> doSomething(s));'
---    
    com.simple.kafka.producer.KafkaProducer      生产者
        sample:
            'KafkaProducer<String, String> producer = new KafkaProducer<>(props).build();'
            'while (true) {
                         producer.sendMsg("test", UUID.randomUUID().toString(), (metadata, exception)
                                 -> callBack()
                     }'
            or:
            self implements `ProducerCallBack`

