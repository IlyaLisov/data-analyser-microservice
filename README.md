# Data analyser microservice

This is data analyser microservice
for [YouTube course](https://www.youtube.com/playlist?list=PL3Ur78l82EFBhKojbSO26BVqQ7n4AthHC).

This application receives data
from [Data generator service](https://github.com/IlyaLisov/data-generator-microservice)
with Apache Kafka.

### Usage

To start an application you need to pass variables to `.env` file.

Application is running on port `8082`.

All insignificant features (checkstyle, build check, dto validation) are not
presented.

#### Example:

```agsl
KAFKA_BOOTSTRAP_SERVERS=localhost:9092
KAFKA_SUBSCRIBED_TOPICS=data-temperature,data-power,data-voltage
```

Just after startup application will try to connect to Apache Kafka and begin to
listen topics from `KAFKA_SUBSCRIBED_TOPICS`.