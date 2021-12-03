# customer_io_WebPortal_BE_API_
customer.io WebPortal_B ackend API
Files Uploaded are:
1.	Postman Installation guide/newman command to run script
2.	Postman collection
3.	Postman environment


Few Observations:
1.	ga_client_id in the Login endpoint is not a mandatory field or needed field Even when it’s taken out of the payload it works. so why was it provided?

2.	When you delete a segment is successfully returning 204 no content. Also, when you delete a segment that was previously deleted, it returns the same response code. in my opinion, i feel both scenarios are different so the response shouldn't act in a similar manner.

3.	create Segment: i can create the same segment multiple times, as a result causing duplicate records.

4.	Type "dynamic" in create segment isn't mandatory is that the expected behaviour

5.	the Field Key in create segment returns a 500 and a 200 ok on 2 test scenarios with no details

6.	Operator key is returning 500 with no details

7.	inverse key is not mandatory, is there any reason for that. does it have a default value configured on the database? just wondering what is getting populated in the DB.

8.	create Type value in request is different in type in response

9.	creating a profile with id as space and email field as empty is returning 202 instead of 422 unprocessable.

10.	Creating profile with existing Id is returning the correct response code and messages. but there is a value that doesn’t seem to have been handled properly.

11.	the response messages for Delete segment is different from delete profile for similar test scenarios. I suggest we standardize across all our APIs

