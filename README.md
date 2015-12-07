# apigee-deploy-now
Deploy Now button for Apigee Edge samples.

[![Deploy to Apigee](./images/deploy_to_apigee.png)](http://http://ec2-52-23-232-127.compute-1.amazonaws.com/login-form/?repo=https://github.com/maruthichand/Mavendeploynow.git&apiFolder=/src/gateway/forecastweatherapi/&makeScript=makeScript.sh)

##### Trigger make API
```shell
curl -X POST -H "Content-Type: application/x-www-form-urlencoded" -d 'repo=https%3A%2F%2Fgithub.com%2Fakoo1010%2Fapigee-tutorials.git' -d 'apiFolder=apiproxies%2Fapigee-nock-mock' -d 'makeScript=make.sh' \
-d 'org=testmyapi' -d 'env=test' -d 'userName='$ae_username'' -d 'pw='$ae_password'' 'http://localhost:3000/deploy' -v
```

##### Access Login App
http://localhost:3000/login-form/

##### Access resources generated by make file
All builds will be created under ```builds/{org}-{env}``` folder.
http://localhost:3000/builds/testmyapi-test/README.md

**Note: ae_username and ae_password can be replaced with an actual username and password.**
