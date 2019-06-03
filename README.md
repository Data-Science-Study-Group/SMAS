Smart Meter Data Analysis System - SMAS
======================

Figure 1 shows the architecture of SMAS, which consists of real-time layer, batch layer and analytics layer. The real-time layer consumes raw smart meter data and runs simple alerting queries, such as those which detect very high consumption readings.  The batch layer packages raw data into chunks that are batch-loaded into the analytics database, e.g., once an hour or once a day.  The batch layer also accepts bulk-uploads, e.g., historical consumption data from legacy systems.  Thus far, we have implemented the analytics layer (see Figure 2), which consists of an underlying database, analytics libraries, and a Web front-end. The analytics layer uses PostgreSQL as the database,  MADLib (madlib.net) as the (in-database) machine learning library,  Highcharts (www.highcharts.com) as the visualization engine, and Tomcat as the web application server. 
![The architecture of SMAS](https://raw.githubusercontent.com/xiufengliu/SMAS/master/src/main/webapp/img/meter3.png)

The functionalities:
============================
This system is still under development. The current implementation has the following functionalities:

* *Consumption time series analytics;*
* *Consumption profiling;*
* *Pattern discovery;*
* *Segmentation (clustering) analysis;*
* *Consumer feedback;*
* *Forecasting*



Installation & Usage
===========================
To use SMAS, users first have to install the open source RDBMS [PostgreSQL](http://www.postgresql.org/), the in-database machine learning toolkit, [MADlib](www.madlib.net), the open source application server [Tomcat](http://tomcat.apache.org/). Then, run the the sql script to create the smas database, schema, tables and the analytics functions.

When the above steps are done, run the gradlew to compile the the source codes, deploy the generated binary packages, and start the application, etc.


Video
======================
[Here](https://www.youtube.com/watch?v=5717mOJSwfI&list=UU9F0rInEDHm1RiFD_R_TGMQ) is the video of introducing SMAS.

Publication
========================

1. X. Liu, L. Golab, I. F. Ilyas. SMAS: A Smart Meter Data Analysis System (demo). Proc. of the 31st International Conference on Data Engineering (ICDE), pp. 1476-1479, 2015. [PDF](https://www.dropbox.com/s/1jcpwlxif8zq2k6/SMAS.pdf?dl=0) 
2. X. Liu, and P. S. Nielsen. Streamlining Smart Meter Data Analytics. In Proc. of the 10th Conference on Sustainable Development of Energy, Water and Environment Systems, SDEWES2015.0558, 1-14, 2015. [PDF](http://orbit.dtu.dk/fedora/objects/orbit:140092/datastreams/file_707af3a3-492d-40cc-81eb-65a3b860fb90/content)
