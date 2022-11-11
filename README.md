# B2C-Commerce-Postman-Collections-Environments
Repo contains useful B2C Commerce Postman Calls for "educational / learning" purpose.

For playing around with `OCAPI endpoint` calls, you can directly download the **OCAPI demo.postman_collection.json** & **OCAPI Env Vars.postman_environment**


********************************************************************************************************************

`Headless / SCAPI endpoint` collection contain:
- **Regular SCAPI** calls (product, coupon, etc)
- **Einstein API** calls 
- **Zone API** calls 
- **STG eCDN API** calls. 

Hence, download **Headless NEW API's.postman_collection.json** collection and import into your Postman workspace.

a) For using normal SCAPI calls (product, coupon, etc) you can use **Headless Env Vars.postman_environment.json**

b) For using Einstein / eCDN Zone APIs, I would recommend you to download **Einstein Headless Environment.postman_environment.json** as it has our BDLW test environment.

c) For using Staging eCDN APIs, kindly download **eCDN STG Environment.postman_environment.json**


To make this solution work for your Commerce Cloud Sandbox, do the following:

Update shortCode, OrganizationID & ClientID as per your environment on the collection. Clone the API clients from the collection(s) and create new one for you.

When you run a specific API endpoint, ensure that you add it's "SCOPE" in the body of OAuth2 BM Token Auth call.

Example: For calling Product API endpoint, we need to append scope ("sfcc.products.rw")

Under Key & value in Headers of the request add the below respectively

`scope` & `SALESFORCE_COMMERCE_API:{{tenant}} sfcc.products.rw`

********************************************************************************************************************



For playing around with `SLAS endpoint` calls, you can directly download the **SLAS Shopper API.postman_collection.json** & **SLAS Env Vars.postman_environment.json**


For using the `Cloduflare APIs`, follow the DOC for generating the API Token which need to be used as Bearer Token and you can use my **Cloudflare API.postman_collection.json** as reference.




**NOTE**: These are purely for “educational” purpose, you can download the collection(s) & environment(s) but, I request all of you to kindly modify the environment with respective Client IDs, Client Secrets & environment scopes. 




**Useful Docs:**

- https://documentation.b2c.commercecloud.salesforce.com/DOC1/topic/com.demandware.dochelp/OCAPI/current/usage/OpenCommerceAPI.html
- https://documentation.b2c.commercecloud.salesforce.com/DOC1/topic/com.demandware.dochelp/OCAPI/current/usage/OAuth.html?resultof=%22%4f%43%41%50%49%22%20%22%6f%63%61%70%69%22%20%22%61%75%74%68%22%20

- https://developer.commercecloud.com/s/commerce-api-apis
- https://developer.salesforce.com/docs/commerce/commerce-api/guide/auth-z-scope-catalog.html

- https://developer.salesforce.com/docs/commerce/commerce-api/guide/slas.html
- https://developer.salesforce.com/docs/commerce/commerce-api/references/shopper-login?meta=Summary

- https://api.cloudflare.com/
