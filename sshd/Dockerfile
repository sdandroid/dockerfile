FROM       ubuntu:16.04
RUN apt-get update
RUN apt-get install -y openssh-server
RUN mkdir /var/run/sshd

RUN echo 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDjyxTTHfUbpdJ+1Ia/ba+HsjMZhITD7Am5rKFW0B9k4vrzi4RfYUpuky5K0bJ1Dx95qW6ZtFMKtMzIVISfORIsGvooghpoEFZQmLjyozsCdMttVU9QxBWDit+tCXXXTOwAYr7rruLn7GM0oTK3JXKMoDHkHi5tyCD5gj/mQVnsMFUwcPZNKcRsdbDjBY4SlklI3m6NYoIz8NaO+QjEQtviiiH+WRo3GXfz+u9HSyi36WFKY5t3s3YdJVfYXRRyGF4bD2Ue8BEW4tjiUxZOwFox5W+9oRXAZDzwkwioSMoUeQE5OImv1ku8MVFkXGmrU7OU3KZgQmYRzUhz23qEgk/3 root@8156e916cefd' > /root/authorized_keys

RUN chmod 644 /root/authorized_keys

RUN sed -ri 's/^PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -ri 's/PasswordAuthentication yes/#PasswordAuthentication yes/g' /etc/ssh/sshd_config

EXPOSE 22

CMD    ["/usr/sbin/sshd", "-D"]
