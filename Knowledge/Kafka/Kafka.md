[[Kafka]] is a distributed log committer which can be used for asynchronous communication where the upstream and downstream services are to be decoupled and scaled independently.

Key Components:
Brokers:
	Central servers which listens for producers and consumers reqs and performs the log appending or retrieval along with offset management, schema registry etc.
[[Producer]]:
	Upstream service which which produces data and sends to brokers for appending to the disk of kafka.
[[Consumer:]]
	Downstream service which reads the messages from the kafka by provinding the offset to the particular kafka topic and partition assignment is done by special broker called Consumer group coordinator.
Own Kafka implementation Github URL: (https://github.com/KarunyaReddyJ/Distributed-log-committer)
Blog of explanation https://karunya-blog.vercel.app/blog/understanding-kafka-from-first-principles