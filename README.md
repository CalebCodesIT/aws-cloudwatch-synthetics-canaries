## Cloudwatch Synthetics

https://us-west-2.console.aws.amazon.com/cloudwatch/home?region=us-west-2#synthetics:canary/list?~
https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries.html
https://www.youtube.com/watch?v=MItluIsvfTo

This is a code first IDE approach to creating, testing and deploying canaries.

By modularizing each AWS resource, resources can be reused, if a large amount of canaries are needed.

These resources can be shared across canaries, so that duplicate resources are not needed:

- vpc
- vpc subnets
- canary vpconfig
- security group (with outbound egress only - the minimum needed)
- IAM role used by the lambda (Selenium)
- Alarms
- SNS topic connected to Slack
- S3 bucket with subfolders for each canary
- runconfig
- schedule
- synthetics group (for grouping canaries)

---
The canaries are written in code and can be version controlled.

The canaries are deployed via Cloudformation

to the cloudwatch synthetics service. The canaries are run on a schedule
and the results are stored in cloudwatch logs.

The canaries can be monitored using cloudwatch alarms.

---
utils are provided to pull logs and view local in an IDE.

AWS Artifacts Deployed
-- link

---
Reference: