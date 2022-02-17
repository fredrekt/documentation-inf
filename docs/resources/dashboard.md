---
sidebar_position: 3
---

# Dashboard

Dashboard/Backoffice access is based on off its sub domain for its user roles.

<strong>User Roles</strong>

1. [Operator](https://admin.infinitegamings.com)
2. [Root](https://root.infinitegamings.com)
3. [Branch](https://branch.infinitegamings.com)
4. [Distributor](https://distributor.infinitegamings.com)
5. [Store](https://store.infinitegamings.com)


Your credentials per account is provided on the excel sheet: Credentials. It wont work unless you match your subdomain to your user role.

## Modules


<strong>Datatables</strong>:

They can either be role based or plainly just operator/admin role.

```bash

var axios = require('axios');

var config = {
  method: 'post',
  url: `https://${api_uri}/dashboard-deposit-requests`,
  headers: { }
};

axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});

```


<strong>Operator Functions</strong>:

Super admin of the backoffice/dashboard, requires Authentication/Authorization.

```bash

var axios = require('axios');
var qs = require('qs');
var data = qs.stringify({
  'role': 'admin' 
});
var config = {
  method: 'post',
  url: 'https://testapi.infinitegamings.com/dashboard-event-bonus-total',
  headers: { 
    'Authorization': '${type of auth} ${authToken}', 
    'Content-Type': 'application/x-www-form-urlencoded'
  },
  data : data
};

axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});

```
<strong>note</strong>: content types can be any.<br/> <br/>

<strong>Multi Level Marketting</strong>:
Also known as Partner Management, where all the magic happens the Commission Points Distribution per win or bet amount of the player. Refer to binary tree below:

![Partner Management Binary Tree](../assets/images/mlm.png) <br/>

<strong>Note</strong>: Advisable to go through the backend first to get the full gist of the endpoints used in dashboard/backoffice.

## Misc
Everything on dashboard's page view's layout is based on user role as well. Contact Lead Developer for more clarification.
