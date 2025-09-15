Prerequisites
--------------
1) CodeStar Connection => Replace ARN to Root Yaml files
2) Replace Default Parameter value from Root Yaml
3) Create SSM parameter - DEV / STG / UAT/ PRD
4) Create Secret Manager (DB username and password) - DEV / STG / UAT/ PRD => (replace ARN in Root Yaml)

CloudFormation Stack Steps
-----------------------------
1) Upload Stack files  =>  replace s3 URL to corsponding Stack URL
2) Upload Root Stack


Stack Parameter Default Value
-----------------------------
- CodeStarConnectionARN 
- FERepositoryId
- BERepositoryId
- GitHubBranch
- AlarmEmail
- DBSecretArn

SSM Parameter
-------------
- /todo-app/dev/VITE_API_BASE_URL (String)
- /todo-app/dev/DATABASE_URL (Secure String)


Post Stack Creation Action
--------------------------
1) Add FE URL to CORS Configuration
2) Replace DATABASE_URL , VITE_API_BASE_URL to SSM parameter