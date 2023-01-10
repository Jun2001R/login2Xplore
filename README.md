# Student Enrollment Form
### Input groups in the project
1. Roll no. as Primary key
2. First Name and Last Name 
3. Class 
4. Date of Birth 
5. Address 
6. Enrollment Date
We took data from javaScript by elementId.val() (not used post method in form) and  made a request which can be send for database for write operation (PUT Command) and finally with the help of token, Data is saved in DataBase.
Also for fetching the data from Database GET_BY_KEY command has been used.
For updating data from database UPDATE command has been used. 
### Benefits of JsonPowerDB
1. Serverless support to use database
2. Schema free
3. No Sql Queries used
4. Multimode dataBase
5. Easy to Use and handle
### Release History
 var updatedData=createUPDATERecordRequest("90932449|-31949270577190091|90955362",JSON.stringify(jsonStrObj),"STUDENT-TABLE",
                "SCHOOL-DB", localStorage.getItem("rec_no") )
                jQuery.ajaxSetup({ async: false });
                 var response = executeCommandAtGivenBaseUrl(
                updatedData,
                "http://api.login2explore.com:5577",
                "/api/iml"
            );
            jQuery.ajaxSetup({ async: true });
      ###
            
    var getRequest = createGET_BY_KEYRequest(
                "90932449|-31949270577190091|90955362",
                "STUDENT-TABLE",
                "SCHOOL-DB",
                JSON.stringify(jsonStrObj),
                true,
                true
            );
            jQuery.ajaxSetup({ async: false });
            var studentData = executeCommandAtGivenBaseUrl(
                getRequest,
                "http://api.login2explore.com:5577",
                "/api/irl"
            );
            jQuery.ajaxSetup({ async: true });
            
           ### 
   var putRequest = createPUTRequest(
                    "90932449|-31949270577190091|90955362",
                    JSON.stringify(jsonStrObj),
                    "STUDENT-TABLE",
                    "SCHOOL-DB"
                );
                jQuery.ajaxSetup({ async: false });
                executeCommandAtGivenBaseUrl(
                    putRequest,
                    "http://api.login2explore.com:5577",
                    "/api/iml"
                );
                jQuery.ajaxSetup({ async: true });
