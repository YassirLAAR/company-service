# company-service
Spring boot project for CRUD operations about companies
this project use this configuration service:

[service-config](https://github.com/YassirLAAR/service-config "service-config")

### How to run correctly

#### Run the service-config app

Check how here in this [README.md](https://github.com/YassirLAAR/service-config#readme "service-config")
If you're using eclise, go to the class **CompanyServiceApplication** and run it as JavaApplication

#### Testin the app in a browser 

In a browser, use this url to get the configuration used in the company-service:
* http://localhost:8081/myConfig
```json
{
   "me":"yassir.laaroussi@outlook.com",
   "yParam":862,
   "threadName":"http-nio-8081-exec-3",
   "xParam":687
}
```

Update the configuration file used in the service-config:

old application.properties:

    yParam=862
    me=yassir.laaroussi@outlook.com
    server.port=8081
    

new application.properties:

    yParam=8859
    me=yassir.laaroussi@outlook.com
    server.port=8081
    

Using the application **Advanced REST client** in google chrome to send a post call to the app.
*http://localhost:8081/actuator/refresh
Send a Post Request 
![Post Request](https://github.com/YassirLAAR/service-config/blob/master/PostRequest.png)
The Post response 
![Post Response](https://github.com/YassirLAAR/service-config/blob/master/PostResponse.png)

Back to the browser, refresh the page to see the new configuration:
* http://localhost:8081/myConfig
```json
{
   "me":"yassir.laaroussi@outlook.com",
   "yParam":8859,
   "threadName":"http-nio-8081-exec-3",
   "xParam":687
}
```
