FROM ubuntu:focal-20201106
RUN apt-get update -y && apt-get install -y python3-pip python-dev libpq-dev git curl tree
RUN git clone https://github.com/endocode/LCV-CM.git
WORKDIR "/LCV-CM"
RUN make
WORKDIR "/LCV-CM/src/LCV"
EXPOSE 8080

ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]

# CMD ["python3","LCVServer.py"]
