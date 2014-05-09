Installation on Windows Server
==============================

Core requirements
-----------------

* Web server that supports PHP integration (Apache HTTPD, Microsoft IIS, nginx with PHP-FPM etc.)
* PHP >= 5.3.7
* MCrypt PHP Extension
* PDO-MySQL PHP Extension
* OpenSSL PHP Extension
* MySQL Server >= 5.5
* Redis Server (Requires special setup on Windows servers. See Redis installation section).

Redis installation
------------------

Redis isn't officially supported on Microsoft Windows but a stable port has been made by Microsoft Open Tech. Using this
along with the RedisWatcher application can be used to run Redis as a serviceon Windows.

Below are the steps needed to set-up Redis on Windows:

1. Download and extract the Redis binaries from the `2.6 branch`_.
2. Copy all extracted binaries to c:\redis\bin.
3. Create another folder at c:\redis\inst1.
4. Download and extract the RedisWatcher binaries from the 2.4 branch.
5. Run InstallWatcher.msi. This should create a Windows service called Redis watcher.
6. Open up the Windows Services console and start the Redis watcher service.
