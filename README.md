# ioc-generic-templated

This IOC or IOC template is or was generated from https://github.com/pcdshub/ioc-generic-templated .

Please update this readme with information about your IOC!

The intended use of this template is as a starting point for a new hutch-specific IOC that builds from any of our common templates.

You can create a new IOC and pick this as a template to help you get started.


## Naming

If your common IOC repository called ioc-common-iocname, and you're creating an IOC for area, then your new IOC repository should be called ioc-area-iocname on github.
You can make exceptions to this if you have good reasons to.

When you clone your IOC from github, feel free to put it in any folder you want.
When we deploy your IOC it will be placed in a directory structure like ioc/area/iocname, but during development this is not needed.
I recommend cloning your repository as-is unless you have a specific more comfortable way to work on these.


## Cfg files

The template is expecting to use your .cfg files to build specific instances of the common IOC.
It should result in a build directory that contains standard iocBoot directories.

All cfg files are expected to point to a specific directory path as the variable "RELEASE",
after which there are various sorts of specifiers that can be used to parameterize the IOC.

Here is an example IMS ioc config file from XCS (with the engineer's name scrubbed for privacy):

```
RELEASE=/reg/g/pcds/epics/ioc/common/ims/R6.0.0
ARCH=rhel7-x86_64
ENGINEER=My Buddy (mbuddy)
LOCATION=XCS:XXX

MOTOR(NAME=XCS:USR:MMS:17,PORT=digi-xcs-17:2101)
MOTOR(NAME=XCS:USR:MMS:18,PORT=digi-xcs-17:2102)
MOTOR(NAME=XCS:USR:MMS:19,PORT=digi-xcs-17:2103)
MOTOR(NAME=XCS:USR:MMS:20,PORT=digi-xcs-17:2104)
MOTOR(NAME=XCS:USR:MMS:21,PORT=digi-xcs-17:2105)
MOTOR(NAME=XCS:USR:MMS:22,PORT=digi-xcs-17:2106)
MOTOR(NAME=XCS:USR:MMS:23,PORT=digi-xcs-17:2107)
MOTOR(NAME=XCS:USR:MMS:24,PORT=digi-xcs-17:2108)
MOTOR(NAME=XCS:USR:MMS:25,PORT=digi-xcs-17:2109)
MOTOR(NAME=XCS:USR:MMS:26,PORT=digi-xcs-17:2110)
MOTOR(NAME=XCS:USR:MMS:27,PORT=digi-xcs-17:2111)
MOTOR(NAME=XCS:USR:MMS:28,PORT=digi-xcs-17:2112)
MOTOR(NAME=XCS:USR:MMS:29,PORT=digi-xcs-17:2113)
MOTOR(NAME=XCS:USR:MMS:30,PORT=digi-xcs-17:2114)
MOTOR(NAME=XCS:USR:MMS:31,PORT=digi-xcs-17:2115)
MOTOR(NAME=XCS:USR:MMS:32,PORT=digi-xcs-17:2116)
MOTOR(NAME=XCS:USR:MMS:33,PORT=mcc-xcs-01:2101)
MOTOR(NAME=XCS:USR:MMS:34,PORT=mcc-xcs-01:2102)
MOTOR(NAME=XCS:USR:MMS:35,PORT=mcc-xcs-01:2103)
MOTOR(NAME=XCS:USR:MMS:36,PORT=mcc-xcs-01:2104)
MOTOR(NAME=XCS:USR:MMS:37,PORT=mcc-xcs-01:2105)
MOTOR(NAME=XCS:USR:MMS:38,PORT=mcc-xcs-01:2106)
MOTOR(NAME=XCS:USR:MMS:39,PORT=mcc-xcs-01:2107)
MOTOR(NAME=XCS:USR:MMS:40,PORT=mcc-xcs-01:2108)
MOTOR(NAME=XCS:USR:MMS:41,PORT=mcc-xcs-02:2101)
MOTOR(NAME=XCS:USR:MMS:42,PORT=mcc-xcs-02:2102)
MOTOR(NAME=XCS:USR:MMS:43,PORT=mcc-xcs-02:2103)
MOTOR(NAME=XCS:USR:MMS:44,PORT=mcc-xcs-02:2104)
MOTOR(NAME=XCS:USR:MMS:45,PORT=mcc-xcs-02:2105)
MOTOR(NAME=XCS:USR:MMS:46,PORT=mcc-xcs-02:2106)
MOTOR(NAME=XCS:USR:MMS:47,PORT=mcc-xcs-02:2107)
MOTOR(NAME=XCS:USR:MMS:48,PORT=mcc-xcs-02:2108)
```
