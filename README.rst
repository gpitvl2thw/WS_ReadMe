########################################
Williams-Sonoma Inc. [Selenium Tests]
########################################

This repository contains `Selenium <http://seleniumhq.org/>`_ tests for the `Williams-Sonoma Inc. <http://www.williams-sonoma.com/>`_, `GitHub Account <https://github.com/YuriiChukhrai/WS_Base>`_.


    .. image:: https://github.com/YuriiChukhrai/WS_Base/blob/master/screenshot/ws.jpg
        :alt: Williams Sonoma
        :width: 30%
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
Run
=============
To run the framework using basic options and their syntax:

``mvn [clean] [test/site] [-DdriverType=FF] [-Denv=prod/qa] [-Ptest1/-Ptest2/-Ptest3] [-Dtestngfile=testng_xml_file]``

----------------
Clean
----------------
To clean the folders from test data from the previous run use the command [clean]

``mvn clean``

----------------
Run test without/with of report
----------------
To run the framework for execution you need to choose the desired option [test/site]

~~~~~~~~~~~~
Run test without of report
~~~~~~~~~~~~
To run tests without getting a report use option test

``mvn clean test``

~~~~~~~~~~~~
Run test with of report
~~~~~~~~~~~~
To run tests with getting a report use option site

``mvn clean site``

----------------
Browser
----------------
To run the framework in a particular browser, to need to specify the name of the browser as a parameter of the option of [-DdriverType]

~~~~~~~~~~~~
Firefox
~~~~~~~~~~~~
To run in Firefox use -DdriverType=FF, below:

``mvn clean site -DdriverType=FF/ff/FIREFOX/FireFox/firefox/FOX/Fox/fox``

~~~~~~~~~~~~
Chrome - [Not Implement yet]
~~~~~~~~~~~~
To run in Chrome use -DdriverType=CHROME, below:

``mvn clean site -DdriverType=CH/ch/CHROME/chrome/GOOGLE/google``

~~~~~~~~~~~~
Internet Explorer - [Not Implement yet]
~~~~~~~~~~~~
To run in Internet Explorer use -DdriverType=IE, below:

``mvn clean site -DdriverType=IE/ie``

~~~~~~~~~~~~
Default
~~~~~~~~~~~~
If you don't specify this parameter, default option -DdriverType = HtmlUnitDriver

``mvn clean site -DdriverType=FF``

----------------
Environment or Production
----------------
In order to specify the run mode, production or environment specify the desired option [-Denv]

~~~~~~~~~~~~
Environment
~~~~~~~~~~~~
To run in production mode, use option qa - [Not Implement yet]

``mvn clean site -Denv=qa``

~~~~~~~~~~~~
Production
~~~~~~~~~~~~
To run in production mode, use option prod

``mvn clean site -Denv=prod``

~~~~~~~~~~~~
Default
~~~~~~~~~~~~
If you don't specify this parameter, default = qa

``mvn clean site -Denv=qa``

----------------
Profile
----------------
In order to use a profile to run tests specify the desired option [-Ptest1/-Ptest2/-Ptest3]

~~~~~~~~~~~~
Profile #1
~~~~~~~~~~~~
Use option -Ptest1 to run the default profile

* if you specify a profile -Ptest1, then the following option [-Dtestngfile=testng_TestsTemp0_Title.xml] should not be specified.

~~~~~~~~~~~~
Profile #2
~~~~~~~~~~~~
Use option -Ptest2 to run the profile where to need specify just testng_xml_file use option [-Dtestngfile=testng_TestsTemp0_Title.xml]

~~~~~~~~~~~~
Profile #3
~~~~~~~~~~~~
Use option -Ptest3 to run the profile where to need specify full path and testng_xml_file use option [-Dtestngfile=!testngxml!/testng_TestsTemp0_Title.xml]

~~~~~~~~~~~~
Default
~~~~~~~~~~~~
If you don't specify this parameter default option profile = -Ptest1

* if you specify a profile -Ptest1, then the following option [-Dtestngfile=testng_TestsTemp0_Title.xml] should not be specified.

----------------
TestNG file
----------------
If specified the previous option, it is necessary to specify what of file need to run test, specify the option [-Dtestngfile=testng_xml_file]

testng_All.xml

testng_All_OneMethod.xml

testng_TestsTemp0_Title.xml

testng_TestsTempI_Account_All.xml

testng_TestsTempI_Account_OneMethod.xml

testng_TestsTempII_All.xml

testng_TestsTempII_OneMethod.xml

=============
OPEN REPORT
=============

In project exist 3 kind of reports:

----------------
SureFire report
----------------
The `SureFire <http://maven.apache.org/surefire/maven-surefire-plugin/>`_ Plugin is used during the test phase of the build lifecycle to execute the unit tests of an application.

~~~~~~~~~~~~
Open report
~~~~~~~~~~~~
To open the browser and in the address bar enter the path:

``.\target\site\surefire-report.html``

    .. image:: https://github.com/YuriiChukhrai/WS_Base/blob/master/screenshot/testng_TestsTemp0_Title.jpg
        :alt: github circuit board illustration
        :width: 30%
        :align: center

----------------
Allure report - [Not Implement yet]
----------------
`Allure <http://allure.qatools.ru/>`_ is open-source framework designed to create test execution reports clear to everyone in the team. 

~~~~~~~~~~~~
Open report
~~~~~~~~~~~~
[Not Implement yet]

----------------
Java Code Coverage report - [Not Implement yet]
----------------
`JaCoCo <http://www.eclemma.org/jacoco/index.html>`_ is a free code coverage library for Java, which has been created by the EclEmma team based on the lessons learned from using and integration existing libraries for many years. 

~~~~~~~~~~~~
Open report
~~~~~~~~~~~~
[Not Implement yet]

