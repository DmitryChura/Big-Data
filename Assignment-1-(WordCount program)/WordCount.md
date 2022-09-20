Run the WordCount program Instructions.  
Start the Cloudera VM in VirtualBox and open a browser:  
![Image text](https://github.com/DmitryChura/Big-Data/blob/main/screenshots/browser.png)  
I use "Pirates.txt" file. Enter link https://raw.githubusercontent.com/DmitryChura/Big-Data/main/Assignment-1-(WordCount%20program)/Pirates.txt in the browser and click "Open menu"->"Save page" and save as "Pirates.txt" in Downloads:  
![Image text](https://github.com/DmitryChura/Big-Data/blob/main/screenshots/save%20page.jpg)  

Open a terminal shell. Commands we use:  
- use "cd Downloads" to go to the Downloads directory  
- run "hadoop fs -copyFromLocal Pirates.txt" to copy the text file to HDFS
- run "hadoop fs -ls" to verify the file was copied to HDFS
- run "hadoop jar /usr/jars/hadoop-examples.jar wordcount Pirates.txt outFile"
- run "hadoop fs -ls outFile" to look inside "outFile"
- run "hadoop fs -copyToLocal outFile/part-r-00000 results.txt"
- run "more results.txt" to view the contents of the results  

![Image text](https://github.com/DmitryChura/Big-Data/blob/main/screenshots/runs.jpg)  

We can see results, for example, how many times does the word "ELIZABETH" occur:

![Image text](https://github.com/DmitryChura/Big-Data/blob/main/screenshots/Results.jpg)
