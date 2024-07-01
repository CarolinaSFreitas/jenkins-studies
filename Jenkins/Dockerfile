FROM jenkins/jenkins

USER root
RUN apt-get update && apt-get -y install lsb-release
RUN apt -y install lsb-release apt-transport-https ca-certificates
RUN wget -0 /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
RUN echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list 

RUN apt-get update && apt-get -y install php7.4 php-mbstring php-xml php-bcmath php-zip php-curl php-mysql php-sqlite3 php-xdebug php-xmlrpc php-soap php-intl php-gd php-imagick php-redis php-memcached php-ldap php-ssh2 php-pear php-dev

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

