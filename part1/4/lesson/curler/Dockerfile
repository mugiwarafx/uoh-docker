FROM ubuntu:20.04
WORKDIR /usr/src/app
COPY script.txt .
RUN apt-get update && apt-get install -y curl 
# CMD ./script.sh
ENTRYPOINT ["./script.txt"]