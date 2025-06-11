# "The Command Line Murders"

**Scenario**:  
This is the Command Line Murders with a small twist as in the solution is different.

**Level**: Easy  
**Type**: Do  
**Tags**: bash  

**Description**:  
This is the Command Line Murders with a small twist as in the solution is different.  
Enter the name of the murderer in the file `/home/admin/mysolution`, for example `echo "John Smith" > ~/mysolution`.  
Hints are at the base of the `/home/admin/clmystery` directory. Enjoy the investigation!

**Root (sudo) Access**: False  

**Test**:  
`md5sum ~/mysolution` returns `9bba101c7369f49ca890ea96aa242dd5`  
(You can always see `/home/admin/agent/check.sh` to see how the solution is evaluated).
