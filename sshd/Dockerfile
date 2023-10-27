FROM  ubuntu:22.04
RUN apt-get update \
&& apt-get install -y openssh-server curl \
&& mkdir /var/run/sshd && mkdir /root/.ssh && chmod -R 700 /root/.ssh \
&& sed -ri 's/^PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config \
&& sed -ri 's/#PasswordAuthentication yes/PasswordAuthentication no/g' /etc/ssh/sshd_config \
&& sed -ri 's/#AuthorizedKeysFile/AuthorizedKeysFile/g' /etc/ssh/sshd_config

EXPOSE 22

CMD    ["/usr/sbin/sshd", "-D"]
