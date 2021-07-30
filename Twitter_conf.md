# Twitter Agent conf File

## create a conf file
  ```
  touch flume-conf
  ```
 ## paste the following code in the conf file
  ```
  TwitterAgent.sources = Twitter 
  TwitterAgent.channels = MemChannel 
  TwitterAgent.sinks = HDFS

  TwitterAgent.sources.Twitter.type = org.apache.flume.source.twitter.TwitterSource
  TwitterAgent.sources.Twitter.channels=MemChannel

  TwitterAgent.sources.Twitter.consumerKey =  1K7mz1LdWUsASdZPS7E4NbZx9
  TwitterAgent.sources.Twitter.consumerSecret = VH60cHfooph4yPec5h7Wwx51vMbKo65I4BDIgNye5ofT0W2tj4
  TwitterAgent.sources.Twitter.accessToken =   837610788747624448-2ByD43M4D8C6XVsfGeBfM083bGrbBql
  TwitterAgent.sources.Twitter.accessTokenSecret = 2wL2LcMWeEnGR0JQ12OKbxvInNDeMWI9vQVua26qtSP48
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
