# c2c_timezone


c2c_timezone(Convert to client timezone) is a simple yet useful JS that is used to convert the time to the client side timezone by employing minimum changes  in your application. c2c_timezone is capable to convert the  date-time to both local and any other timezone you want it to. 

This package has **javascript handle** that can be fetched into your code to handle the date objects. The primary purpose of this package is to eliminate the mundane code that user  uses to handle timezones and necessary formats.

The package could be used for following cases:
- **Convert the date from server to local (host or browser) time.**
- **Convert the date from server to ANY standard timezone(IANA) offset you want it to be.**



## Usage

 1.**To convert a date by using a data attribute**
    
   Return the date in the following format :
     
   `<div data-ctoc-timezone   data-ctoc-time="" data-ctoc-req-zone="" data-ctoc-req-format=""</div>`
   
   Here **data-ctoc-timezone** is the identifier for attribute,  gets removed once the date is conversion is complete.
   
   **data-ctoc-time** is the time to be converted , should be given in a valid JS date-string  format . **[View Date String formats]**  (https://pages.github.com/).
   
   **data-ctoc-req-zone** is the timezone to convert the given date-time object.The field accepts all IANA timezones and variety of other timezone offsets. You can also give the offset in form of **"+hh:mm" or "-hh:mm" or simply an integer**.The Timezone offsets are available in the **[View Time Zones]**  (https://pages.github.com/).
   
   **data-ctoc-format** is the format specifier for the date-time object. You can construct your own format using the following rules       **[View Formats](https://pages.github.com/)**. Not defining the format gives a Date with Datestring format.
   
   **Example** :
   
   `<div data-ctoc-timezone  data-ctoc-time="Mar 01 2013 05:30:00 +5:30" data-ctoc-req-zone="" data-ctoc-req-format=""></div>`
    
   Output:
   
    `Fri Mar 01 2013 05:30:00 GMT+0530 (India Standard Time)`
   
   **For Changing Timezone :**
   - Using IANA format:
   
   `<div data-ctoc-timezone  data-ctoc-time="Mar 01 2013 05:30:00 +5:30" data-ctoc-req-zone="America/Lima" data-ctoc-req-format=""></div>`
    
  Output :
  
  `Thu Feb 28 2013 19:00:00`
   
   - Using offset in hh:mm format:
   
   `<div data-ctoc-timezone  data-ctoc-time="Mar 01 2013 05:30:00 +5:30" data-ctoc-req-zone="-5:00" data-ctoc-req-format=""</div>`
Output :
  `hu Feb 28 2013 19:00:00`
  
 -Using Integer :
  
  
  
                                
   
 2.**To convert any date object in JS on client side** Include a div tag in the html code in following format 
    
   `<div data-ctoc-timezone="" data-ctoc-time="" data-ctoc-req-zone="" data-ctoc-req-format=""</div>`
    Example:
    `<div data-ctoc-timezone="server" data-ctoc-time="Feb 28 2013 19:00:00 EST" data-ctoc-req-zone="IST" data-ctoc-req-format="Do M YYYY        hh:mm:ss a"</div>`
    The above example converts your EST time to IST, and return the date in string.
    
                                                            or
   Call the the `convertTime` function in js.
        `CtoCTimezone.convertTime(dateobject,"Required time zone");`
   Example:
          `CtoCTimezone.convertTime(new Date(),"America/New_York")`;
          


## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc


