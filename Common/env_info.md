# Pivotal Cloud Foundry Environments

**Contents**
- [PCF Environments](#pcf-environment-information)
- [Logging into an environment](#logging-into-an-environment)
- [Marketplace information](#marketplace-information)

## PCF Environment Information
Use the following information to connect (login) to specific environments as directed by the instructor.

### Pivotal Web Services (PWS)
- Website: http://run.pivotal.io
- Endpoint: api.run.pivotal.io
- Username: Typically your email used when creating your PWS account
- Password: From your account
- Use [PWS Marketplace services](#pws-marketplace-services-and-plans) below

### Pivotal Google Cloud Platform
- Website: https://apps.sys.calistoga.cf-app.com
- Endpoint: api.sys.calistoga.cf-app.com
- Username: Assigned by instructor --> `user1` through `user4`
- Password: Assigned by instructor
- Use [GCP Marketplace services](#gcp-marketplace-services-and-plans) below

## Logging into an Environment
Using the above information, your step to login are as follows below. When logging in, PCF will ask you for your password and which PCF Space, i.e. development, test, or production, in which you would like to work. Spaces can always be changed later using `cf target -s test`, for instance.

```
$ cf login -a <endpoint> -u <user> --skip-ssl-validation
```

For PWS, for instance, use the following with the appropriate user:
```
$ cf login -a api.run.pivotal.io -u user1 --skip-ssl-validation
API endpoint: api.run.pivotal.io
...
```

Or for GCP, use the user# you were assigned.

```
$ cf login -a api.sys.calistoga.cf-app.com -u user1 --skip-ssl-validation
API endpoint: api.sys.calistoga.cf-app.com
...
```

With both of the above commands, PCF will request and authenticate your password then ask which `org` and `space` to target. If only one `org` and `space` exist, then the target will automatically be set for you.

```
...
Password>
Authenticating...
OK

Targeted org user1-org

Select a space (or press enter to skip):
1. development
2. test
3. production

Space> 1
Targeted space development

API endpoint:   https://api.sys.calistoga.cf-app.com (API version: 2.54.0)
User:           user1
Org:            user1-org
Space:          development
```

## Marketplace Information
Depending upon the PCF environment in which you are connected, the following Marketplace Services and Plans are available. For instance, if you are instructed to create a new 100mb MySQL service instance while using the PWS environment, then use the following:

```
$ cf create-service p-mysql 100mb mydb
```

Otherwise, for the GCP environment, use the following:

```
$ cf create-service p-mysql 100mb-dev mydb
```

### PWS MarketPlace Services and Plans
Service Name | Plans | Description
------------ | ----- | -----------
app-autoscaler | bronze, gold | Scales bound applications in response to load (beta)
cleardb | spark, boost*, amp*, shock* | Highly available MySQL for your Apps.
cloudamqp | lemur, tiger*, bunny*, rabbit*, panda* | Managed HA RabbitMQ servers in the cloud
p-circuit-breaker-dashboard | standard | Circuit Breaker Dashboard for Spring Cloud Applications
p-config-server | standard | Config Server for Spring Cloud Applications
p-mysql | 100mb, 1gb, 20gb | MySQL databases on demand
p-service-registry | standard | Service Registry for Spring Cloud Applications
rediscloud | 100mb*, 250mb*, 500mb*, 1gb*, 2-5gb*, 5gb*, 10gb*, 50gb*, 30mb | Enterprise-Class Redis for Developers

### GCP Marketplace Services and Plans
Service Name | Plans | Description
------------ | ----- | -----------
app-autoscaler | bronze, gold | Scales bound applications in response to load (beta)
p-circuit-breaker-dashboard | standard | Circuit Breaker Dashboard for Spring Cloud Applications
p-config-server | standard | Config Server for Spring Cloud Applications
p-mysql | 100mb-dev | MySQL service for application development and testing
p-rabbitmq | standard | RabbitMQ is a robust and scalable high-performance multi-protocol messaging broker.
p-redis | shared-vm, dedicated-vm | Redis service to provide a key-value store
p-service-registry | standard | Service Registry for Spring Cloud Applications

[Course Materials home](/README.md#course-materials)
