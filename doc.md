
## A - Solr URLs

1. Solr Master (For Creatives)

http://ws-solr-master01:9085/solr/

2. Solr Slave 02 (For creatives)

http://ws-solr-slave01:9085/solr/

3. olr Slave 01 (For creatives)

http://ws-solr-slave02:9085/solr/

4. Solr Master (For Geo and Airings/Occurrence except TV)

http://ws-solr-geomaster01:8085/solr/

5. Solr Slave (For Geo and Airings/Occurrence except TV)

http://ws-solr-geoslave01:8085/solr/

6. Solr Master (For TV Airings)

http://ws-solr-geomaster01:8086/solr/

7. Solr Slave (For TV Airings)

http://ws-solr-geoslave01:8086/solr/

## B - Load Balancer (This sits in front of ws-solr-slave01 and ws-solr-slave02)

This one has to be up for website searches to work.

http://webutil01:81/solr/  (webutil01 used to be called headsup01)

We use haproxy as load balancer. If webutil01 was restarted, there is a cron job for user root that should start haproxy. If haproxy is still down, login to that machine (using any webteam member login) and sudo to root user and execute that cron job.


## C - RabbitMQ URL

http://realtimetvsvr01:15672/

Requires username/password. Use standard bplus account.Then select virtual host from the right corner (for alert, select /alert). Then click on 'Queues' to see any pending messages.

