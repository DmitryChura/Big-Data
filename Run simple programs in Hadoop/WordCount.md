Run the WordCount program Instructions  
Start the Cloudera VM in VirtualBox and open a browser  
картинка браузера  
I use "Pirates.txt" file. Enter link https://raw.githubusercontent.com/DmitryChura/Big-Data/main/Run%20simple%20programs%20in%20Hadoop/Pirates.txt in the browser and click "Open menu"->"Save page" and save as "Pirates.txt" in Downloads 
фото сохранения  
Open a terminal shell. Commands we use:  
- use "cd Downloads" to go to the Downloads directory  
- run "hadoop fs -copyFromLocal Pirates.txt" to copy the text file to HDFS
- run "hadoop fs -ls" to verify the file was copied to HDFS
- run "hadoop jar /usr/jars/hadoop-examples.jar wordcount Pirates.txt outFile"
- run "hadoop fs -ls outFile" to look inside "outFile"
- run "hadoop fs -copyToLocal outFile/part-r-00000 results.txt"
- run "more results.txt" to view the contents of the results  
фото runs
