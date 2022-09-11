# Data-Pipeline2-dsti

Below instruction are provided based on Ubuntu OS

    • how to clone the github project
      1. Login to github
      2. Move to main branch ,click on code dropdown and copy hyperlink from there
      3. Open terminal , move to required folder where cloning needs to be done
      4. run below command
        git clone "copied git clone hyperlink"
        
    • how to run the batch using the maven/mill command locally
      For development, maven is used insted of mill. To run code from intellij using maven, follow below instructions.
        1. Add below parameters in intellij Config argument
          1. For generating new_brazil_covid19.csv
            path for brazil_covid19_cities.csv
            path for brazil_covid19.csv
            path where new_brazil_covid19.csv has to be saved
          2. For generating report
            path for brazil_covid19.csv
            path for new_brazil_covid19.csv
            path where report-diff.json to be saved
            
    • how to package automatically the jar file 
      1.  Import project using Intellij and use maven "mvn clean compile package" command to generate jar file
      
    • how to run the batch using the spark-submit command locally (considering spark home is configured in path)
      1. for new_brazil_covid19.csv
         spark-submit  \
         --class com.spark.scala.job.MainDriver \
         path_to_jar/MAIN_DRIVER.jar \
         path for brazil_covid19_cities.csv \
         path for brazil_covid19.csv \
         path where new_brazil_covid19.csv has to be saved
         
    • how to run the batch using the spark-submit command with AWS 
    • how to generate the diff report locally (considering spark home is configured in path)
         spark-submit  \
         --class com.spark.scala.job.Report \
         path_to_jar/MAIN_DRIVER.jar \
         path for brazil_covid19.csv
         path for new_brazil_covid19.csv
         path where report-diff.json to be saved
    
    new_brazil_covid19.csv link : https://github.com/jailakwale/Data-Pipeline2-dsti/blob/main/src/main/resources/new_brazil_covid19.csv
    report-diff.json link : https://github.com/jailakwale/Data-Pipeline2-dsti/blob/main/src/main/resources/report-diff.json
    
    
   NOTE: Please refer the Project Report.docx
   
   Thank you!
