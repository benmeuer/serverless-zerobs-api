zerobs = scratch

*** Run tests (create/get/list);
  serverless invoke local --function create --path mocks/create-event.json
  serverless invoke local --function get --path mocks/get-event.json
  serverless invoke local --function list --path mocks/list-event.json
  serverless invoke local --function update --path mocks/update-event.json

//###################################################
//###################################################
//###################################################

//============= IAM User ======
zerobs_admin
Access Key ID: AKIASWUXYV54KVUAXLBX
Secret Key: jJcmg9cCYTjlVDWOk53OEBR+GZs4rBa7FPgKQcaa

//============= Dynamo DB =====
TableName: recipes = notes
 * recipeId
 * userId
 * From original example, I changed "content" var to be 2 vars: 
  ** title
  ** content

//============= Cognito =====
Pool Name: zerobs-user-pool
Pool Region: us-east-2
Pool Id: us-east-2_xRFvpFPLf
Pool ARN: arn:aws:cognito-idp:us-east-2:186075623288:userpool/us-east-2_xRFvpFPLf
App Client Name: zerobs-app
App Client Id: 4jknqus205r7kge9578ha4e8ff
Cognito Domain Name: https://zerobs-app.auth.us-east-2.amazoncognito.com
Cognito Test User: testUser@example.com
Cognito Test UserPass: Passw0rd!

//============= Setting up Serverless =====
 * The directory created with the node.js starter command (setting up
   the serverless framework chapter) was notes-app-api.  I changed it
   to be zerobs-api
