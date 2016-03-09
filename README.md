# Twitter-Hashtags-Analyser

/* Version 1.0
A Qlik Sense app that is using Qlik REST Connector to load data from Twitter. Is has some limitation of rows loaded from Twitter.


To use this app in Qlik Sense you need to: 

Download


1. Download Qlik REST API Connector http://market.qlik.com/rest-connector.html


2. Download extension WordCloud https://github.com/cleveranjos/br.com.clever.wordcloud/ or https://community.qlik.com/docs/DOC-7794

Twitter


1. Have or Create an Account on Twitter (for authentication)


Apigee


1. Go to https://apigee.com/console/twitter


2. Choose service https://api.twitter.com/1.1
 

3. Choose authentication OAuth 1 and give access/autorize app to your twitter account
 

4. In left menu "Search" select tweets 
 

5. Then in Query fill in the q field with the hashtag you want to analyse
 

6. Fill in Since ID - the max date from which will be loaded data in some interval to history
 

7. Click on send button
 

8. The data for REST connector will appear in the Request URL and on the left side in Request
 

9. Dont close the website, you will need it for next steps.

Now you have all information needed for Qlik Rest Connector, to create new Qlik Sense connection you need to:
1. Open data load editor and in the right corner click create new connection
 

2. Choose Qlik REST Connector and name the connection to "Twitter hashtag"


3. URL - copy the "Request URL" from Apigee website 


4. Timeout - 30


5. Check autodetect response type and Key generation stragegy - Sequence ID


6. Windows anthentication - NO


7. Your twitter mail and password


8. Use certificatie - NO


9. Pagination type - NO


10. In query headers create 3 rows:
    a. Authorization
    b. Host
    c. X-Target-URI


11. Copy the information from Apigee (you can find it by clicking on Send button in apigee and after the server response, 
	they will appear on the left side in Request.


12. Test conection    


13. In the sheet Twitter_user you have load script


14. Now you can Load data or preview the data.


15. Thats all!

Enyoj!

Maros
