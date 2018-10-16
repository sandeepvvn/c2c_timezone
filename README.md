# c2c_timezone


c2c_timezone(Convert to client timezone) is a simple yet useful JS that is used to convert the time to the client side timezone by employing minimum changes the in your application. c2c_timezone is capable to convert the server time to both local and any other timezone you want it to. 

This package has **javascript handle** that can be fetched into your code to handle the date objects. The primary purpose of this package is to eliminate the mundane code that user has to use to handle timzones and necessary format.

The package could be used for following cases:
1. **Convert the date from server to local (host or browser) time.**
2. **Convert the date from server to ANY standard timezone(IANA) offset you want it to be.**



## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.



### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo


## Usage

 1.**To convert a date by using a div tag**
    
   Return the date in the following format :
     
     `<div data-ctoc   data-ctoc-time="" data-ctoc-req-zone="" data-ctoc-req-format=""</div>`
   
   Here **data-ctoc** is the identifier for tag, which gets removed once the date is converted.
   
   **data-ctoc-time** is time to be converted which should be given JS date string  format . **[View Date String formats]**  (https://pages.github.com/).
   
   **data-ctoc-req-zone** is the timezone you want the time to be converted.The field accepts all IANA timezones and variety of timezone offsets. You can also give the offset in form of "+hh:mm" or "-hh:mm" or simply an integer.( The Timezone codes are available in the **[View Time Zones]**  (https://pages.github.com/).
   
   **data-ctoc-format** is supplement which returns date required in a specified format which you desire.There are a range format it supports **[View Formats](https://pages.github.com/)**.Not defining the format gives a Date with Datestring format.
   
   Example :
   
   `<div data-ctoc-timezone  data-ctoc-time="Mar 01 2013 05:30:00 +5:30" data-ctoc-req-zone="" data-ctoc-req-format=""</div>`
    
   Output:
   
    `Fri Mar 01 2013 05:30:00 GMT+0530 (India Standard Time)`
   
   For Changing Timezone :
   1.Using IANA format:
   
   `<div data-ctoc-timezone  data-ctoc-time="Mar 01 2013 05:30:00 +5:30" data-ctoc-req-zone="America/Lima" data-ctoc-req-format=""</div>`
    
  Output :
  
  `Thu Feb 28 2013 19:00:00`
   
   2. Using offset in hh:mm format:
   
   `<div data-ctoc-timezone  data-ctoc-time="Mar 01 2013 05:30:00 +5:30" data-ctoc-req-zone="-5:00" data-ctoc-req-format=""</div>`
Output :
  `hu Feb 28 2013 19:00:00`
  
  3. Using Integer :
  
  
  
                                
   
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


