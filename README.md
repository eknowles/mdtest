#Index

**Classes**

* [class: AirWatchService](#AirWatchService)
  * [new AirWatchService(config)](#new_AirWatchService)
  * [airWatchService.makeRequest(url, post, callback)](#AirWatchService#makeRequest)
  * [airWatchService.updateVersion(options)](#AirWatchService#updateVersion)
  * [airWatchService.installApp(options, callback)](#AirWatchService#installApp)
  * [airWatchService.uploadAppBlob(filename, callback)](#AirWatchService#uploadAppBlob)
  * [airWatchService.uploadAppChunks(filename, callback)](#AirWatchService#uploadAppChunks)
  * [airWatchService.getDeviceApps(options, callback)](#AirWatchService#getDeviceApps)
  * [airWatchService.getDeviceInfo(options, callback)](#AirWatchService#getDeviceInfo)
  * [airWatchService.getDeviceCertificates(options, callback)](#AirWatchService#getDeviceCertificates)
  * [airWatchService.getDeviceCompliance(options, callback)](#AirWatchService#getDeviceCompliance)
  * [airWatchService.getDeviceContent(options, callback)](#AirWatchService#getDeviceContent)
  * [airWatchService.getDeviceProfiles(options, callback)](#AirWatchService#getDeviceProfiles)
  * [airWatchService.getDeviceEventLog(options, callback)](#AirWatchService#getDeviceEventLog)

**Functions**

* [getFilesizeInBytes(filename)](#getFilesizeInBytes)
 
<a name="AirWatchService"></a>
#class: AirWatchService
This is a description of the AirWatchService class.

**Members**

* [class: AirWatchService](#AirWatchService)
  * [new AirWatchService(config)](#new_AirWatchService)
  * [airWatchService.makeRequest(url, post, callback)](#AirWatchService#makeRequest)
  * [airWatchService.updateVersion(options)](#AirWatchService#updateVersion)
  * [airWatchService.installApp(options, callback)](#AirWatchService#installApp)
  * [airWatchService.uploadAppBlob(filename, callback)](#AirWatchService#uploadAppBlob)
  * [airWatchService.uploadAppChunks(filename, callback)](#AirWatchService#uploadAppChunks)
  * [airWatchService.getDeviceApps(options, callback)](#AirWatchService#getDeviceApps)
  * [airWatchService.getDeviceInfo(options, callback)](#AirWatchService#getDeviceInfo)
  * [airWatchService.getDeviceCertificates(options, callback)](#AirWatchService#getDeviceCertificates)
  * [airWatchService.getDeviceCompliance(options, callback)](#AirWatchService#getDeviceCompliance)
  * [airWatchService.getDeviceContent(options, callback)](#AirWatchService#getDeviceContent)
  * [airWatchService.getDeviceProfiles(options, callback)](#AirWatchService#getDeviceProfiles)
  * [airWatchService.getDeviceEventLog(options, callback)](#AirWatchService#getDeviceEventLog)

<a name="new_AirWatchService"></a>
##new AirWatchService(config)
Creates an object of the AirWatchService

**Params**

- config `Object`  
  - username `String` - AirWatch API Username.  
  - password `String` - AirWatch API Password.  
  - groupid `String` - Group ID.  
  - apicode `String` - aw-tenant-code.  
  - host `String` - IP Address or domain name of the AirWatch server.  

**Returns**: [AirWatchService](#AirWatchService)  
<a name="AirWatchService#makeRequest"></a>
##airWatchService.makeRequest(url, post, callback)
Make an request to the AirWatch API

**Params**

- url `string` - Endpoint to make the request, do not include hostname.  
- post `object` - A json object with data to post. Optional.  
- callback `function` - The callback that handles the response.  
  - error `object`  
  - response `object`  
  - body `object`  

<a name="AirWatchService#updateVersion"></a>
##airWatchService.updateVersion(options)
Request the current version of an App and update it via semantic versioning. This is currently designed for iOS apps, must have agvtool installed.

**Params**

- options `Object`  
  - app `String` - Bundle ID of App.  
  - \[status=active\] `String` - Status of App.  
  - \[release=PATCH\] `String` - Type of release.  

<a name="AirWatchService#installApp"></a>
##airWatchService.installApp(options, callback)
Installs an Application on a device

**Params**

- options   
- callback   

<a name="AirWatchService#uploadAppBlob"></a>
##airWatchService.uploadAppBlob(filename, callback)
Upload an App to the AirWatch API as a single Blob

**Params**

- filename `string` - Filename of app. Must be in the same directory (for now).  
- callback `function` - The callback that handles the response.  
  - error `object`  
  - response `object`  
  - body `object`  

<a name="AirWatchService#uploadAppChunks"></a>
##airWatchService.uploadAppChunks(filename, callback)
Upload Application Chunks (iOS and Android).
Uploads application chunks into the AirWatch database for internal application install. This function must be used prior to the 'Begin Install API' for uploading an internal application.

**Params**

- filename `string` - Name of the file you want to upload.  
- callback `string` - Returns a function with the uploaded transactionId.  

<a name="AirWatchService#getDeviceApps"></a>
##airWatchService.getDeviceApps(options, callback)
Returns an object containing an array of applications installed on the device.

**Params**

- options `object` - A json object containing items needed to make the request.  
  - deviceId `string` - Type of identification. Can be either 'macaddress', 'serialnumber' or 'UDID'.  
  - uid `string` - Unique ID of the device. Can be either a valid MAC address, serial number or UDID.  
- callback   

<a name="AirWatchService#getDeviceInfo"></a>
##airWatchService.getDeviceInfo(options, callback)
Retrieves details of the device identified by its numeric ID.

**Params**

- options `object` - A json object containing items needed to make the request.  
  - deviceId `string` - Type of identification. Can be either 'macaddress', 'serialnumber' or 'UDID'.  
  - uid `string` - Unique ID of the device. Can be either a valid MAC address, serial number or UDID.  
- callback   

<a name="AirWatchService#getDeviceCertificates"></a>
##airWatchService.getDeviceCertificates(options, callback)
Retrieves the details of the certificates that are present on the device.

**Params**

- options `object` - A json object containing items needed to make the request.  
  - deviceId `string` - Type of identification. Can be either 'macaddress', 'serialnumber' or 'UDID'.  
  - uid `string` - Unique ID of the device. Can be either a valid MAC address, serial number or UDID.  
- callback   

<a name="AirWatchService#getDeviceCompliance"></a>
##airWatchService.getDeviceCompliance(options, callback)
Retrieves the details of the compliance policies that are present on a device.

**Params**

- options `object` - A json object containing items needed to make the request.  
  - deviceId `string` - Type of identification. Can be either 'macaddress', 'serialnumber' or 'UDID'.  
  - uid `string` - Unique ID of the device. Can be either a valid MAC address, serial number or UDID.  
- callback   

<a name="AirWatchService#getDeviceContent"></a>
##airWatchService.getDeviceContent(options, callback)
Retrieves the details of the content that is present on a device.

**Params**

- options `object` - A json object containing items needed to make the request.  
  - deviceId `string` - Type of identification. Can be either 'macaddress', 'serialnumber' or 'UDID'.  
  - uid `string` - Unique ID of the device. Can be either a valid MAC address, serial number or UDID.  
- callback   

<a name="AirWatchService#getDeviceProfiles"></a>
##airWatchService.getDeviceProfiles(options, callback)
Retrieves the profile related information of the device.

**Params**

- options `object` - A json object containing items needed to make the request.  
  - deviceId `string` - Type of identification. Can be either 'macaddress', 'serialnumber' or 'UDID'.  
  - uid `string` - Unique ID of the device. Can be either a valid MAC address, serial number or UDID.  
- callback   

<a name="AirWatchService#getDeviceEventLog"></a>
##airWatchService.getDeviceEventLog(options, callback)
Retrieves the event log details of the device.

**Params**

- options `object` - A json object containing items needed to make the request.  
  - deviceId `string` - Type of identification. Can be either 'macaddress', 'serialnumber' or 'UDID'.  
  - uid `string` - Unique ID of the device. Can be either a valid MAC address, serial number or UDID.  
- callback   

<a name="getFilesizeInBytes"></a>
#getFilesizeInBytes(filename)
Returns a filesize in bytes of a file.

**Params**

- filename   

**Returns**: `number` - bytes - Total file size in bytes.  
