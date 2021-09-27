Home Assignment 

Hi everyone,

I have created ios app as per the home assignment information.


I am able to setup mock server and able to receive messae from browser.


Browser Output

http://localhost:8080/

{"status":"success","description":"Server running well!","availableRoutes":["/authenticate/login","/account/balances","/account/transactions","/account/payees","/transfer"]}
I am able to execute the  POST, GET requests in the postman.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

However while trying connect thru simulator received the below issues.

The error message have received after receive response in the xcode

TestApp[54242:2308891] [] nw_socket_output_finished [C1.1:2] shutdown(9, SHUT_WR) [57: Socket is not connected]


Error Message - Received in the terminal while execute the request from Xcode.


Error [ERR_HTTP_HEADERS_SENT]: Cannot set headers after they are sent to the client
    at ServerResponse.setHeader (_http_outgoing.js:561:11)
    at ServerResponse.header (/Users/rajkumar/2021/25092021/node_modules/express/lib/response.js:771:10)
    at ServerResponse.send (/Users/rajkumar/2021/25092021/node_modules/express/lib/response.js:170:12)
    at ServerResponse.json (/Users/rajkumar/2021/25092021/node_modules/express/lib/response.js:267:15)
    at ServerResponse.send (/Users/rajkumar/2021/25092021/node_modules/express/lib/response.js:158:21)
    at /Users/rajkumar/2021/25092021/build/routes/auth.js:21:14
    at Layer.handle [as handle_request] (/Users/rajkumar/2021/25092021/node_modules/express/lib/router/layer.js:95:5)
    at next (/Users/rajkumar/2021/25092021/node_modules/express/lib/router/route.js:137:13)
    at Route.dispatch (/Users/rajkumar/2021/25092021/node_modules/express/lib/router/route.js:112:3)
    at Layer.handle [as handle_request] (/Users/rajkumar/2021/25092021/node_modules/express/lib/router/layer.js:95:5)


I have crearted JSON responses from the Postman tool for further client implementation.

Using the Response JSON file the client has developed.


1) User is able to login (Mock response file)
2) User is able to see the balances / transactions in the account  (Mock response file)
3) User is able to retrieve his/her list of payees (Mock response file)
4) User is not able to make a tranfer

In the Postman Response below message received, using that response JSON file has created.

{
    "status": "failed",
    "description": "Invalid request"
}





