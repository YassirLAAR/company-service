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
![Post Request](https://uc386a4c8710536d6f63be6b07ef.previews.dropboxusercontent.com/p/thumb/ABPT3TXuS1F3LYmZwfe2JXHrzhhCrXht9jI10BUfX22jPBx6HYPVBwk_96FS0cuAtNGxJj7fJKbboLvrkPvQ9hidEi4t5vmQkohTFG8eSeH8T6MQSrobCkQQST1UrxArsUr7XqbhiWcHN3xrqGcDRJe0y8BEX8euHST5iS5QO085bpzQs-TFdLT60UAJd05RsuQ9g_Gc-qA3fVnEPDmYO-sFSEOVwzoaQlltZk1rqKu2fQcETQoAAQnLEZDGRJ9e9vK5keoCRRuw1fyttoOJytIaNo9byQFS_Uy_KScLI4Pld1n_lJrnncd79GAmnUORurkURKMvap5tT4tDDGllRbZBWsbOrNJy65-04FG4cHMees0ARaEjgMXHU8ml1SSCXk7zc-BsOJ1CHGxAT-_0Naz_/p.png?fv_content=true&size_mode=5)
The Post response 
![Post Response](https://uc7488d6a15475cab955e3943c6c.previews.dropboxusercontent.com/p/thumb/ABPZuWYG5WuUUNJms0YZaDe80bpS5fpuY-Jc1FlxxZcki4olXQf3Sn1AxWXNvpZHiHHTSu6XHuXmiTpVHwIY83moHvrRotrIkNGJVKJHsNFHtcWwEmtCxMGLbz2lNiwxlvEmNeFlBAAZPos4GerOUq142Mte0TRWq-I1KyptpwnJL1ZzyInLzDQJQr9DVJlTkyV30PQXaQugiH0-CAkzHvgUhWd-ySTG7q13LsYE5LAXpcP_B3qkDFV9CEFlX4wqym1H5xDwmHqhEwtIFI-FwhpuB84WefbRwnR8qn4iU_yHkzq2pqI79E1FkEisxPNwYEDfM8c7AcyNJx0RS1uS-104l-JKU0dTian5ga5eODDdIQysLaG15480QKO8-44ExjmJ4Nc4YuyWu2_rxU25WioH/p.png?fv_content=true&size_mode=5)

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
