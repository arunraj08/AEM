#Create custom Log File in AEM
-------------------------------
1) Navigate to sling > Log support.
    http://localhost:4502/system/console

2)Click on add new logger button at the bottom of the top panel.
   Enter log file: logs/training.log and logger: apps.training.

3)Save changes.

##Adding Logger in JS:
-------------------------
1) Add log.info method and add the message to print in log fle.
   Ex :  log.info("#####Current Page Title : " + root.getTitle());


2) when you open any page from your application, this script will run and create an entry in the trainin log flie. You can find this log file in the crx-quickstart-log folder.

##Adding Logger in Java File:
-----------------------------
1) Import the Logger and LoggerFactory class in java file
     
    Ex: import org.slf4j.Logger;
        import org.slf4j.LoggerFactory;

2) Create Logger object from the LoggerFactory.getLogger() method.
    Ex: Logger log= LoggerFactory.getLogger(TopNav.class);

3) Invoke logger.info() method with some message.
    Ex: log.info(" Test Log with Logger Helper");

