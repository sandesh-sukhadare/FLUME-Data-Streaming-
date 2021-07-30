# Twitter Agent conf File

## Create a conf file
  ```
  touch flume-conf
  ```
 ## Paste the following code in the conf file
  ```
  TwitterAgent.sources = Twitter 
  TwitterAgent.channels = MemChannel 
  TwitterAgent.sinks = HDFS

  TwitterAgent.sources.Twitter.type = org.apache.flume.source.twitter.TwitterSource
  TwitterAgent.sources.Twitter.channels=MemChannel

  TwitterAgent.sources.Twitter.consumerKey =  Enter your consumerKey here
  TwitterAgent.sources.Twitter.consumerSecret = Enter your consumerSecret here
  TwitterAgent.sources.Twitter.accessToken =   Enter your accessToken here
  TwitterAgent.sources.Twitter.accessTokenSecret = Enter your accessTokenSecret here
  
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
