# athento-nx-comments

## Operation Document.CreateComment
input params:
type "string" name "comment" - Comment to include to the document
type "string" name "User" - User that makes the comment

### Example

HttpResponse<String> response = Unirest.post("http://barclaycard.athento.com/nuxeo/site/automation/Document.CreateComment")
  .header("authorization", "Basic ** Authorization **")
  .header("content-type", "application/json")
  .header("accept", "application/json+nxentity, */*")
  .header("x-nxdocumentproperties", "*")
  .body("{\"input\":\"** DocID of the Document itself **\",\"context\":{} , \"params\" : {\"comment\" : \"This is my comment\", \"user\" : \"Administrator\"}\n    \n}")
  .asString();


## Operation Document.GetAllComments
input params: none

### Example

HttpResponse<String> response = Unirest.post("http://barclaycard.athento.com/nuxeo/site/automation/Document.GetAllComments")
  .header("authorization", "Basic ** Authorization **")
  .header("content-type", "application/json")
  .header("accept", "application/json+nxentity, */*")
  .header("x-nxdocumentproperties", "*")
  .body("{\"input\":\"** DocID of the Document itself **\",\"context\":{} , \"params\" : {}\n    \n}")
  .asString();

## Operation Document.DeleteComment
input params: 

type "string" name "commentToDelete" - Comment to delete, identified by its docid

### Example

HttpResponse<String> response = Unirest.post("http://barclaycard.athento.com/nuxeo/site/automation/Document.DeleteComment")
  .header("authorization", "Basic ** Authorization **")
  .header("content-type", "application/json")
  .header("accept", "application/json+nxentity, */*")
  .header("x-nxdocumentproperties", "*")
  .body("{\"input\":\"** DocID of the Document itself **\",\"context\":{} , \"params\" : {\"commentToDelete\" : \"** Comment to delete, identified by its docid **\"}\n    \n}")
  .asString();
