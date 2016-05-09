# athento-nx-comments

## Operation Document.CreateComment
input params:
type "string" name "comment" - Comment to include to the document
type "string" name "User" - User that makes the comment
### Example

HttpResponse<String> response = Unirest.post("http://myinstance.com/nuxeo/site/automation/Document.CreateComment")
  .header("authorization", "Basic AUTHORIZATIONREQUIRED")
  .header("content-type", "application/json")
  .header("accept", "application/json+nxentity, */*")
  .body("{\"input\":\"--DOCID---\",\"context\":{} , \"params\" : {\"comment\" : \"Here goes the comment\", \"user\" : \"User-that-makes-the-comment\"}\n    \n}")
  .asString();
