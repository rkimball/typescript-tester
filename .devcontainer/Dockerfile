FROM ubuntu:22.04

# Set frontend to non-interactive so time zone setup does not ask questions
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update --fix-missing && \
    apt-get install -y \
        python3 \
        python3-pip \
        python-is-python3 \
        git \
        vim \
        curl \
        jq

RUN pip install --upgrade pip
RUN pip install octoai-sdk

COPY .devcontainer/aws_config /root/.aws/config
COPY . /usr/app
WORKDIR /usr/app

CMD ["bash"]