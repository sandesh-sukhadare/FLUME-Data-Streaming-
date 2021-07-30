# FLUME-Data-Streaming
Realtime data streaming using flume


### Installing flume on linux (Ubuntu)
1. Download flume tar file
   ```
   wget https://mirrors.ocf.berkeley.edu/apache/flume/1.9.0/apache-flume-1.9.0-bin.tar.gz
   ```
2. Extract the tar file
   ```
   tar xzf apache-flume-1.9.0-bin.tar.gz
   ```
3. Set the FLUME_HOME path in the .bashrc file
   ```
   nano ~/.bashrc
   ```
   ```
   #Flume
   export FLUME_HOME=/home/<"username">/apache-flume-1.9.0-bin
   export PATH=$PATH:/home/<"username">/apache-flume-1.9.0-bin/bin
   ```
4. Save the .bashrc file and exit 
   ```
   {press ctrl+s then ctrl+ x}
   ```

5. Source .bashrc file
   ```
   source .bashrc
   ```

6. Check flume version to verify installation
   ```
   flume-ng version
   ```


