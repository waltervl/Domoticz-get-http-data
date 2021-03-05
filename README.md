# Domoticz-get-http-data

This html file placed in your domoticz server will give a value of your domoticz device as plain text. This can be used in other web based applications to use these values.

Instruction:
* Save getvalue.html file in domoticz/www/views
* Change the line with $.domoticzurl="http://IP-of-server:port"; to the correct IP adress and port of your domoticz server
* Use the following link http://IP-of-server:port/views/getvalue.html?idx=xxx&type=yyy to get the requested value as plain text
  * idx is the idx number of the device
  * type (case sensitive!) is the type of the requested value from the json of your idx device (http://<IP-of-server>:<port>/json.htm?type=devices&rid=idx) like from below example :

* type=Data will give 3.14 (the data is cleaned by the html file)
* type=BatteryLevel will give 255

If the page cannot read a value due to for example type error it will give the value ??

# Example Json data

    {
	"ActTime" : 1614199414,
	"AstrTwilightEnd" : "20:01",
	"AstrTwilightStart" : "05:43",
	"CivTwilightEnd" : "18:44",
	"CivTwilightStart" : "07:00",
	"DayLength" : "10:37",
	"NautTwilightEnd" : "19:23",
	"NautTwilightStart" : "06:21",
	"ServerTime" : "2021-02-24 21:43:34",
	"SunAtSouth" : "12:52",
	"Sunrise" : "07:34",
	"Sunset" : "18:10",
	"app_version" : "2020.2 (build 12901)",
	"result" : 
	[
		{
			"AddjMulti" : 1.0,
			"AddjMulti2" : 1.0,
			"AddjValue" : 0.0,
			"AddjValue2" : 0.0,
			"BatteryLevel" : 255,
			"CustomImage" : 0,
			"Data" : "3.14 Watt",
			"Description" : "",
			"Favorite" : 0,
			"HardwareDisabled" : false,
			"HardwareID" : 8,
			"HardwareName" : "ZiGate",
			"HardwareType" : "Zigate plugin",
			"HardwareTypeVal" : 94,
			"HaveTimeout" : false,
			"ID" : "00158d00032d3827",
			"LastUpdate" : "2021-02-24 21:42:55",
			"Name" : "ZiGate - Power-00158d00032d3827-02",
			"Notifications" : "false",
			"PlanID" : "1",
			"PlanIDs" : 
			[
				1
			],
			"Protected" : false,
			"ShowNotifications" : true,
			"SignalLevel" : 9,
			"SubType" : "Electric",
			"Timers" : "false",
			"Type" : "Usage",
			"TypeImg" : "current",
			"Unit" : 23,
			"Used" : 1,
			"XOffset" : "0",
			"YOffset" : "0",
			"idx" : "113"
		}
	],
	"status" : "OK",
	"title" : "Devices"
}
