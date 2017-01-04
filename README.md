## Description

Show how to deploy a sample PHP application on AWS Elastic Beanstalk using AutoScaling, LoadBalancer, and a pre-existing ElastiCache (memcached) cluster for PHP session storage. The required EC2 instances will be created within a pre-existing VPC and subnets.

## Requirements

You need to install the **Elastic Beanstalk Command Line Interface** (EB CLI) - [See the instructions][1].

## Steps to deploy

1. Clone

	```
	git clone https://github.com/jweyrich/aws-demo-php-eb-elasticache.git
	cd aws-demo-php-eb-elasticache
	```

2. Configure required details

 a) Edit VPC/EC2 details on `.ebextensions\01_instance.config`;
 
 b) Edit the ElastiCache host on `.ebextensions\04_memcached.config`;
 
 c) Add and commit your changes:

	```
    git commit -a -m 'My changes.'
    ```

3. Deploy

	```
	eb deploy
	```

  [1]: http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html