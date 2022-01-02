# for mac use home brew
brew install redis

redis-server

redis-cli

# commands
set name kyle
get name
del name

exists name //does this key exist
keys * //gets all 
flushall
clear 

expire name 10
ttl name //time til it expires

setex name 10 kyle  //sets name to expire in 10 seconds

lpush friends john   //pushes to a list on left
rpush friends sally //pushes to the end of array on right
lrange friends 0 -1 //range from index 0 to -1 (all)
lpop friends //pops off left side
rpop friends //pops off right side

# sets 
sadd hobbies "weight lifting"  //uses sets for unique keys, quotation for string with multiple words
smembers hobbies //gets members from set
srem hobbies "weight lifting" // to remove

# hashes
hset person name kyle
hget person name
hgetall person
hset person age 26
hdel person age
hexists person name
hexists person age