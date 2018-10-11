# c2c_timezone
c2c_timezone(Convert to client timezone) is a simple yet useful **gem** that is used to convert the time to the client side timezone by employing minimum changes the in your application. c2c_timezone is capable to convert the server time to both local and anyother timezone you want it to. 

This package has both **rails and javascript handle** that can be fetched into your code to handle the date objects. The primary purpose of this package is to eliminate the mundane code that user has to use to handle timzones and necessary format.

The package could be used for following cases:
1. **Convert the date from server to local (host or browser) time.**
2. **Convert the date from server to ANY standard timezone(IANA) offset you want it to be.**
3. **Convert time to above  which is in part-reload(instaLoad).**


## Installation:

## Usage:

#### Convert to Local time:
No change required to convert it to local time zone.
` def ctoc_timezone (insta_load=false, run_call_back_script=false, call_back_script="", req_zone="",req_format="" ) `
    
### Convert to any Timezone :

For Example 
