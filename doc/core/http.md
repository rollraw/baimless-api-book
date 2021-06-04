# HTTP table

> Description: functions to make http, https requests and take responses from them

## Functions

 \#\#\# Get Parameters: \| Name \| Type \| Description \| \| :-------- \| :----- \| :----------------------- \| \| szUrlLink \| string \| URL-link for GET request \| Returns: \| Type \| Description \| \| :----- \| :--------------- \| \| string \| request response \| Code: \`\`\`lua local szResponse = HTTP.Get\("https://www.google.com"\) print\(szResponse\) \`\`\` \# \#\#\# Post Parameters: \| Name \| Type \| Description \| \| :----------- \| :----- \| :------------------------ \| \| szUrlLink \| string \| URL-link for POST request \| \| szPostFields \| string \| fields for POST request \| Returns: \| Type \| Description \| \| :----- \| :--------------- \| \| string \| request response \| Code: \`\`\`lua local szResponse = HTTP.Post\("https://www.google.com/search", "q=example"\) print\(szResponse\) \`\`\`

