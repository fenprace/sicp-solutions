FROM debian:stable
EXPOSE 8888
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y build-essential libssl-dev libffi-dev libzmq5 python3 python3-pip python3-dev racket
RUN pip3 install --no-input jupyterlab
RUN raco pkg install --auto iracket && \
    raco pkg install --auto sicp && \
    raco iracket install
CMD jupyter-lab --allow-root --ip 0.0.0.0
