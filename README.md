Broker
======

A broker server for the nodejs implementation of the iLab Shared Architecture

###Purpose
The new service broker provides a vastly different service from the original MIT broker. All student interaction, such as authentication and client software, has been moved into a separate service (see [Agent](https://github.com/ShadovvMoon/Agent)). The new purpose of a service broker is to bridge communication between JSON and SOAP (for legacy MIT batched lab servers). 

The service broker provides a global administration to control access to lab servers. This is useful when you have several [agents](https://github.com/ShadovvMoon/Agent) with different permissions.

The most basic broker converts JSON into SOAP and then sends it directly to the lab server. With the introduction of [nodejs Lab servers](https://github.com/ShadovvMoon/Lab), the most basic broker can simply forward JSON directly to the lab server. Additional caching or other logic may be incorporated through plugins.

###Installation
```
cd <path to broker directory>
npm install
node index.js
```

Open a web browser and navigate to [http://localhost:8080](http://localhost:8080). Login with the username and password **admin** and **password** respectively. Click the Admin drop down menu in the upper right hand corner and then select My Account. Enter **password** as the old password, then type in a new password and click Save.
