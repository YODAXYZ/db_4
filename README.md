# db_4

# 1_lesson_hw
https://docs.google.com/document/d/14GUD3L__DR7NozgrD9-I8VDppZIiqeMAgNzkbiUXVK0/edit

1) Change .aws/credentials
2) Create 3 virtual machine 
aws ec2 run-instances --image-id ami-0817d428a6fb68645 --count 3 --instance-type t2.medium --key-name cassandra --security-group-ids sg-0a8c13e2f2c687ccf --subnet-id subnet-fa9ff8f4
3) Connect to this ec2
4) Install jdk and casandra and check status 

sudo apt install default-jdk

echo "deb http://downloads.apache.org/cassandra/debian 40x main" | sudo tee -a /etc/apt/sources.list.d/cassandra.sources.list

curl https://downloads.apache.org/cassandra/KEYS | sudo apt-key add -

sudo apt-get update

sudo apt-get install cassandra

nodetool status

5) ping 172.31.75.221 check for ping

6) Change /etc/cassanddra/cassanddra.yaml in 3 ec2 

seed_provider:
        - seeds: "172.31.65.98,172.31.75.221,172.31.73.97" #all notes
listen_address: 172.31.65.98 #note in which we are
rpc_address: 172.31.65.98 note  #in which we are

7) Change /etc/cassanddra/cassanddra-rackdc.properties # in 3 notes
dc=uk_dc
rack=rack1

8)sudo service cassandra start # start in 3 notes 

9) nodetool status # And you can see all nodes
 BUT ... AAAAAAaaaa


