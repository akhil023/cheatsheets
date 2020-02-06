**kill a python process**

ps -elf | grep python

kill -9 PID

pkill -9 -f <script_name>.py

**kill a process in port 8000**

sudo fuser -k 8000/tcp
