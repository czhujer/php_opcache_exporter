# PHP OPcache exporter

## Overview

prometheus exporter for PHP OPcache stats, written in python.



integration for discovery a send prometheus metrics to zabbix

## Description

Data is fetched from [opcache_get_status()](http://php.net/manual/en/function.opcache-get-status.php) function.

FastCGi variant was tested on CentOS 7 with php-fpm 7.1.

scprape-uri varianta tested with docker and owncloud docker stack.

## Usage

You can just use "--scrape_uri" for scraping from URL/URI or use fast-cgi client

Help on flags:

<pre>
usage: php_opcache_exporter.py [-h] [-p port] [--scrape_uri SCRAPE_URI]
                               [--fhost FHOST] [--phpfile phpfile]
                               [--phpcontent phpcontent] [--phpcode phpcode]
                               [--fport FPORT]

php_opcache_exporter args

optional arguments:
  -h, --help            show this help message and exit
  -p port, --port port  Listen to this port
  --scrape_uri SCRAPE_URI
                        URL for scraping, such as http://127.0.0.1/opcache-
                        status.php
  --fhost FHOST         Target FastCGI host, such as 127.0.0.1
  --phpfile phpfile     A php file absolute path, such as
                        /usr/local/lib/php/System.php
  --phpcontent phpcontent
                        http get params, such as name=john&address=beijing
  --phpcode phpcode     code for execution over fastcgi client
  --fport FPORT         FastCGI port
</pre>

## Author(s)

* Patrik Majer (@czhujer) <patrik.majer.pisek@gmail.com>

## Docs

* https://prometheus.io/docs/concepts/metric_types/

* https://prometheus.io/docs/instrumenting/writing_exporters/

* https://github.com/prometheus/client_python

* https://github.com/RobustPerception/python_examples/tree/master/jenkins_exporter

* https://github.com/lovoo/jenkins_exporter
