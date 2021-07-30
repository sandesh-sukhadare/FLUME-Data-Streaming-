# Twitter Agent conf File

## Create a conf file
  ```
  touch twitter-conf
  ```
 ## Paste the following code in the conf file
  ```
  TwitterAgent.sources = Twitter 
  TwitterAgent.channels = MemChannel 
  TwitterAgent.sinks = HDFS

  TwitterAgent.sources.Twitter.type = org.apache.flume.source.twitter.TwitterSource
  TwitterAgent.sources.Twitter.channels=MemChannel

  TwitterAgent.sources.Twitter.consumerKey =  Enter_your_consumerKey_here
  TwitterAgent.sources.Twitter.consumerSecret = Enter_your_consumerSecret_here
  TwitterAgent.sources.Twitter.accessToken =   Enter_your_accessToken_here
  TwitterAgent.sources.Twitter.accessTokenSecret = Enter_your_accessTokenSecret_here
  
  TwitterAgent.sources.Twitter.keywords=Tokyo2020

  TwitterAgent.sinks.HDFS.channel=MemChannel
  TwitterAgent.sinks.HDFS.type=hdfs
  TwitterAgent.sinks.HDFS.fileType=DataStream
  TwitterAgent.sinks.HDFS.hdfs.path= /user/sandesh/Tokyo2020

  TwitterAgent.sinks.HDFS.writeFormat=Text
  TwitterAgent.sinks.HDFS.batchSize=100

  TwitterAgent.sinks.HDFS.rollCount=100
  TwitterAgent.channels.MemChannel.type=memory
  TwitterAgent.channels.MemChannel.capacity=10000
  TwitterAgent.channels.MemChannel.transactionCapacity = 1000
  ```
  
  ## Start the Agent
    ```
    flume-ng agent -n TwitterAgent -f /"filepath"/twitter.conf
    ```
