## Sending and Reading Messages from Apache Kafka

This repository is a simple application that connect to Apache Kafka, create a topic, send and read messages.

---

### 1. Dependencies

#### 1.1. Python

[Download and install the Python](https://www.python.org/downloads/).

#### 1.2 Pip

[Download and install the Pip](https://pip.pypa.io/en/stable/installing/)

#### 1.3. Docker Desktop

You would require you to install Docker Desktop to create containers for individual microservices. Refer the following links for instructions

- [macOS](https://docs.docker.com/docker-for-mac/install/),
- [Windows 10 64-bit: Pro, Enterprise, or Education](https://docs.docker.com/docker-for-windows/install/),
- [Windows 10 64-bit Home](https://docs.docker.com/toolbox/toolbox_install_windows/).
- You can find installation instructions for other operating systems at: https://docs.docker.com/install/

---

### 2. Instructions

To run any project code, you will have to set up a virtual environment with project dependencies. All of following instructions are to be completed via a terminal/command line prompt.

#### 2.1. Clone the Repository

First you need to clone this repository

```bash
git clone https://github.com/Waelson/Simple-Kafka-Python-Application.git
```

#### 2.2. Install Python Dependencies

This project has two dependencies. It is setting in 'requirements.txt' file. To install dependency use follow command:

```bash
pip install r- requirements.txt
```

#### 2.3. Start Kafka (run on Docker)

Into 'scripts' folder run the following command:

```bash
./start_kafka.sh
```

or

```bash
docker-componse up -d
```

#### 2.3. Running Python Application

The script bellow create a topic if it don't exists. Then, it send and read messages.

```bash
python app_topic.py
```

In this script you can to simulate message producers sync and async

```bash
python app_producer.py
```

The script bellow set a producer with several parameters that impact the producer's performance.

```bash
python app_param_producer.py
```

#### 2.5. Output console

If you did all correctly, you will get an output similarly to image below.

```bash
python app_topic.py
```

<img src="https://raw.githubusercontent.com/Waelson/kafka-python/main/images/output_topic.png">

```bash
python app_producer.py
```

<img src="https://raw.githubusercontent.com/Waelson/kafka-python/main/images/output_producer.png">

#### 2.5. Accessing KafkaDrop

[Kafdrop](https://github.com/obsidiandynamics/kafdrop) is an open source project that allow you visualize informations about your Kafka Cluster. When you start Kafka (step 2.3), you will be running Kafdrop as well. To access it use the URL bellow. Pay attention: There are others tools that allow you manager Kafka Cluster. Please, consider to visit [CMAK - Cluster Manager for Apache Kafka](https://github.com/yahoo/CMAK) for know more about this fantastic tool.

[http://localhost:9000](http://localhost:9000)

<img src="https://raw.githubusercontent.com/Waelson/kafka-python/main/images/output_kafkadrop.png">
