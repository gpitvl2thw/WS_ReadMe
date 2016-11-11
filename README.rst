########################################
Williams-Sonoma Inc. [Selenium Tests]
########################################

This repository contains `Selenium <http://seleniumhq.org/>`_ tests for the `Williams-Sonoma Inc. <http://www.williams-sonoma.com/>`_, `GitHub Account <https://github.com/YuriiChukhrai/WS_Base>`_.


    .. image:: https://github.com/gpitvl2thw/WS_Photo/blob/master/ws.jpg
        :alt: github circuit board illustration
        :width: 100%
        :align: center


.. contents::

.. section-numbering::

.. raw:: pdf

   PageBreak oneColumn



=============
Dependencies
=============
----------------
Git
----------------
Make sure you have `Git <https://git-scm.com/>`_ installed on your system. For check use the commands below:

``git -v``

----------------
GitHub
----------------
Make sure you have access `GitHub Account <https://github.com/YuriiChukhrai/WS_Base>`_:

``git clone https://github.com/YuriiChukhrai/WS_Base``

----------------
Maven
----------------
Make sure you have `Maven <https://maven.apache.org/download.cgi>`_ installed on your system. For check use the commands below:

``mvn -v/version``

----------------
Java
----------------
Make sure you have `Java <http://www.java.com/>`_ installed on your system, if not follow the vendor instructions for installing them on your operating system.

``java -version``

=============
Run the framework
=============
To run the framework using basic options and their syntax:

``mvn [clean] [test/site] [-DdriverType=FF] [-Denv=prod/qa] [-Ptest1/-Ptest2/-Ptest3] [-Dtestngfile=testng_xml_file]``

----------------
Clean repository
----------------
clean - to clean the folders from test data from the previous run use the commands below:

``mvn clean``

----------------
Run all test without/with of reports
----------------
To run the framework for execution you need to choose the desired option

* test - to run tests without getting a report use the commands below:

``mvn clean test``

* site - to run tests with getting a report use the commands below:

``mvn clean site``

----------------
Select a browser
----------------
To run the framework in a particular browser, to need to specify the name of the browser as a parameter of the option of -DdriverType:

* To run in Firefox use -DdriverType=FF, below:

``mvn clean site -DdriverType=FF/ff/FIREFOX/FireFox/firefox/FOX/Fox/fox``
	
* To run in Chrome use -DdriverType=CHROME, below: - [Not Implement yet]

``mvn clean site -DdriverType=CHROME``
	
To run in Internet Explorer use -DdriverType=IE, below: - [Not Implement yet]

``mvn clean site -DdriverType=IE``

----------------
-Denv
----------------
In order to specify the run mode, production or environment specify the desired option -Denv:

* To run in production mode, use -Denv=prod

``mvn clean site -Denv=qa``

* To run in production mode, use -Denv=qa - [Not Implement yet]

``mvn clean site -Denv=qa``

> if you don't specify this parameter, default = qa

>>``mvn clean site -Denv=qa``

----------------
Run with profile
----------------
-Ptest1/-Ptest2/-Ptest3


> if you specify a profile -Ptest1, then the following option should not be specified.

----------------
[-Dtestngfile=testng_xml_file]
----------------



>>All testng files
>>testng_All
>>testng_TestsTemp0_Title
>>testng_TestsTempI_Acc
>>testng_TestsTempII	
>>testng_TestsTempIII
>>testng_TestsTempIV

=============
OPEN REPORT
=============
Open the browser and in the address bar enter the path:
``.\target\site\surefire-report.html``

