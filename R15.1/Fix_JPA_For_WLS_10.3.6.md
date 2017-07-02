### About Oracle Weblogic 10.3.6 JPA2.0 Issues:

The Topic About The Issues :

[http://docs.oracle.com/cd/E23943_01/web.1111/e13720/using_toplink.htm#EJBAD1311](http://docs.oracle.com/cd/E23943_01/web.1111/e13720/using_toplink.htm#EJBAD1311)

---

### Fix It Manually

add the jars into `weblogic10.3.6` preclasspath

- open the weblogic `commEnv.cmd` where you installed
```bash
C:\Oracle\Middleware\wlserver_10.3\common\bin\commEnv.cmd
```

- add `jars` path into the preclasspath
```bash
@echo off
set wls_modules=C:\Oracle\Middleware\modules # here is the weblogic server path you installed
set PRE_CLASSPATH=%wls_modules%\javax.persistence_1.1.0.0_2-0.jar;%wls_modules%\com.oracle.jpa2support_1.0.0.0_2-0.jar
echo PRE_CLASSPATH=%PRE_CLASSPATH%
```

- restart the weblogic server