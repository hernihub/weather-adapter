# Weather service REST adapter
### This is the REST adapter for the Global Weather SOAP-based web-service for the Deloitte recruitment process previous to the interview: it includes the technical specification document, Node code and Mule code.

Instructions to run the project:

1.	NODE
  * Clone the aforementioned repository
  *	Go to weatherExcerciseDockerFile folder and run npm install
  *	Got to weatherExcerciseDockerFile folder and execute build the docker image and run it as a container or, simply run node server.js to start the Weather SOAP WS
2.	MULE EE RUNTIME
  *	Go to https://www.mulesoft.com/lp/dl/mule-esb-enterprise and download Mule ESB enterprise 4.2.0
  *	Unzip the downloaded file to create the folder
 
3.	MULE APPLICATION
  *	Go to weather-rest-adapter/target folder and copy the JAR file weather-rest-adapter.jar into the app folder of the Mule Enterprise Standalone folder unzipped in the previous step	 
  *	Be sure to have JRE or JDK 8 installed
  *	Go to /bin Mule standalone subfolder and run mule.sh in Linux or mule.bat in Windows

4.	THE API
  *	Open postman or simply go to Firefox and navigate to these URLs:
  
       http://localhost:8081/weather-api/v1/weather/city/Melbourne  
       http://localhost:8081/weather-api/v1/airports/Australia  

5.	THE EXCEPTIONS
  *	If the name of the city or of the country is missing, a HTTP 404 status code with the following message will print the resource is not found or the parameter is missing
  *	Any other call to an URL that is registered in the RAML definition and does not conform to the resource pattern, will end up in either bad request HTTP 400 or 404 


### CHALLENGES
I’ve only heard of Mule, never worked with it before; DataWeave expression language was considerably more complex than connectors or flows since I’ve worked a long time ago with Java CAPS enterprise designer and it was just like this, except than it was BPEL. I found some features particularly difficult and good candidates for refactoring in the future by the Mule team, like going into flow XML a lot of the time (when bad requests are returned, there is this <ee:variables> element that is not shown on the graphical flow). I faced this as usual when looking for new technologies viability: research and more research online and common sense, of course, formed through the years. Mule forum was particularly helpful for obvious reasons. I wrote questions and later answered them myself, learning more than expected in the process and putting my humble contribution out there for the community.
It is very powerful, this Mule ESB. Certainly, one can think of as a risky choice since the debacle of ESB back in the SOA era, but they are doing a great job.

I really hope this short exercise convince you guys that I can be a great member of your integration team; I’ve dedicated the majority of my professional career to integration and I really want to be part of such a prestigious employer as Deloitte is.

Thank you.
