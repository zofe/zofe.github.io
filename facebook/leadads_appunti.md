# appunti facebook leadads


https://github.com/facebook/facebook-php-business-sdk

- integrazioni in crm
https://www.inboundhorizons.com/getting-facebook-lead-ads-real-time-data-endpoint-integrating-crm/

- doc facebook 
https://developers.facebook.com/docs/marketing-api/guides/lead-ads/quickstart/webhooks-integration

curl \
  -F "object=page" \ 
  -F "callback_url=https://www.mysite.it/webhook/facebook-lead-ads" \ 
  -F "fields=leadgen" \ 
  -F "verify_token=mytoken" \ 
  -F "access_token=19xxxxx|qUb46PY4EiutQnlOvUOYAQpB708" \ 
  "https://graph.facebook.com/v2.5/19xxxxx/subscriptions"
 
- Receiving Facebook Leads on a Webhook
https://gist.github.com/tixastronauta/0b9c3b409a7ba96edffc
 

- spiegazioni token accesso
https://developers.facebook.com/docs/facebook-login/access-tokens#extending
  
- strumento di testing
https://developers.facebook.com/tools/lead-ads-testing
  
- strumento di debug per ottenere/estendere chiavi di accesso
https://developers.facebook.com/tools/debug/accesstoken/?access_token=xxx&version=v3.0
  
-spiegazioni su ottenimento access-token permanenti
https://stackoverflow.com/questions/17197970/facebook-permanent-page-access-token
https://github.com/axelero/FB-Lead-Ad-Intake
  
