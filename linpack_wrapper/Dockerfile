FROM registry.access.redhat.com/ubi8:latest

RUN dnf install -y --nodocs python3-pip python3-numpy python3-requests python3-numpy
RUN ln -s /usr/bin/python3 /usr/bin/python
RUN mkdir -p /opt/snafu/
COPY . /opt/snafu/
RUN pip3 install --upgrade-strategy=only-if-needed -r /opt/snafu/requirements.txt

RUN curl https://software.intel.com/sites/default/files/managed/cc/19/l_mklb_p_2019.6.005.tgz --output linpack.tgz
RUN tar xzvf linpack.tgz -C /opt
