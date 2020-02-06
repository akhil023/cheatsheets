**Delete one queue:**

localhost

```rabbitmqadmin delete queue name=name_of_queue```

remote host

```rabbitmqadmin --host=HOST --port=443 --ssl --vhost=VHOST --username=USERNAME --password=PASSWORD delete queue name=QUEUE_NAME```

**Delete all queues**

localhost

`rabbitmqadmin -f tsv -q list queues name > q.txt`

`while read -r name; do rabbitmqadmin -q delete queue name="${name}"; done < q.txt`

remote host

`rabbitmqadmin --host=HOST --port=443 --ssl --vhost=VHOST --username=USERNAME --password=PASSWORD -f tsv -q list queues name > q.txt`

`while read -r name; do rabbitmqadmin -q --host=HOST --port=443 --ssl --vhost=VHOST --username=USERNAME --password=PASSWORD delete queue name="${name}"; done < q.txt`
