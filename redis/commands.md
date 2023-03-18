# to connect to docker redis from local machine
docker exec -it redis redis-cli

# interactive redis cli 
redis-cli

# get all keys
KEYS *

# get key with pattern
KEYS *<partOfKey>*

# deleted key 
DEL <keyName>

# delete multiple keys
DEL <keyName1> <keyName2> <keyName3>

# return value and then delete key
GETDEL <keyName>

# set value
SET <keyName> <value>

# get value
GET <keyName>

# delete all keys ASYNC
FLUSHALL ASYNC