# Default Log Files:

- Error.log: Error messages are registered here.
- Access.log: All access request to AEM and repository are registered here. Eg: Who is accessing and what resource are being accessed.
- Audit.log: It provide record of who did what and when.
- Request.log:  Request and response are registered here. Used to analyze/monitor response time, about how long a req. takes.
- Stderr.log: Holds error message generated during AEM startup.
- Stdout.log: This file holds the events during startup. Eg: Setting sling.properties, sling.home, sling.launchpad, HTTP server port=4502 etc.
- History.log: It holds info. about the things you editors do. Eg: Editing, deleting, viewing a page.

# Custom Log File:

- You can also create  your own custom log file for your application to track messages produced by your own application. AEM has implemented Log4j framework which provide an easy logging solution.

- Two pieces of information are required to append an entry to the log file. Log level and message. 

## Log Level:

- Methods of logger include trace(), debug(), warn(), info(), error() etc.

## Message:

- Messages are provided as parmaters to method call.

Ex: log.debug("This is test message");
