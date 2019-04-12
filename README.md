Weblogic - it's an App server running on JVM. These app servers behaves like an extended virtual machine for running applications, transparently handling connections to the database on one side, and, often, connections to the Web client on the other.

# webLogicScripts
These are helpful in managing the weblogic domains, node and managed servers state i.e. i.e. start | run | stop | restart | status.
control_managed_servers       - This python script located at - /users/mwe/cgscripts/py - is responsible to create t3(proprietary protocol of Weblogic) connection to transport information between WebLogic servers and other types of Java programs.
server_control_functions      - This script has the start, stop funcs. which in turn use control_managed_servers.
wls-control                   - This script uses server_control_functions script. Using this script we can start, stop any managed server in any domain by passing as params.
appstop                       - This script stops all middleware services in a host(In every domain, managed servers and finally admin server)
appstart                      - This script starts all middleware services in a host(In every domain, starts admin server, then starts node manager and then starts all managed servers.)
appstatus                     - This script checks status of all managed servers.
admin_map                     - contains list of all domains and their port numbers.
adminstart                    - This scripts just send out mail after starting admin server.
