## Reading Public Data with Insomnia and the ORCID Public API

You  can read data from the ORCID record using the ORCID Public or Member API and a two step authentication to get the tokens you need to access the data.

In this tutorial we will focus on using the free to use software [Insomnia](https://insomnia.rest/) to manage yout API calls, you can just as well do this with swagger or with Curl and you can find documentation in hoow to do tht here and here.


THis Tutorial will make use of the ORCID sandbox, real world integratiion will use the Production servers and endpoints.

What you will need:
1. A working Public or Member  API on Sandbox link to the othert API tutorial and member.orcid article for this.
2. Internets!
3. A browser so you can follow these insturctions
4. An sandbox orcid record you can look up data from. Ljnk to the other tutorial for this.


1. Download the Insomnia APP from https://insomnia.rest/ and install  on you computer Insomnia wortks onMAc PC andLinux.

2. Get your access tokens
Open up Insomnia and click add to start a new request.

Select Patch in the drop down and Give a titile you will rememeber this one is called get auth toke


<PIC>


Slect
PATCH ▼ https://api.myproduct.com/v1/users

Send

Body ▼ OAuth 2 ▼ Query Header Docs
GRANT TYPE
ACCESS TOKEN URL
client id	APP-XXXXXXXXXXXXXXX
CLIENT SECRET	XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX

▼ Advanced Options
SC0PE	/read-public
credentials &	As Basic Auth Header (default)
HEADER PREFIX 0
AUDIENCE©
REFRESH TOKEN
n/a
ACCESS TOKEN
n/a

Client Credentials
https://sandbox.orcid.org/oauth/token

Fetch Tokens
