CasRestBundle
=============

Cas Rest Bundle allows you to authenticate against a CAS server via RESTFUL services. This bundle works with the awesome FosUserBundle.


 Authored by Saud Faisal


Now go into your app/config.yml and do something as follows:

<pre>
main_cas_rest:<br />
    cas_rest_url: https://sso.myserver.com/cas/restapi/tickets<br />
    cas_service_url: https://sso.myserver.com/cas/serviceValidate<br />
    cas_cert: /usr/share/ca-certificates/extra/ca.crt<br />
    cas_local:<br />
    source_dn: <br />
    base_dn:<br />
    service_url:<br />
</pre>

Please nose that you will have to adjust the path for cas_cert as it is located on your machine. 

Also note that as the bundle stands for now, it will first authenticate locally. In the event you are able to log on, everything is fine. 
In the event that the authentication fails, it will then go to the CAS server, and create a local DB user on successful authentication and then log you in. 

Future versions will allow you to customize this experience fully. I wrote this in a hurry so please bear with me 



This bundle is in middle of some cleanup and I will do my best to refactor it further. Also I will be adding tests in future. 

