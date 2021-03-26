# aws Environment Stack 
### Sort Of Template I guess 🤷‍♂️

This is a starter environment stack, it contains the minimal components I tend to want in an aws account that I use, replace the `_DOMAIN_` with the target domain and complete the stack. This is meant to be a re-usable base but needs some manual work to make this useful, but this is a decent start for a copy paste when bootstraping a new project.

Maybe next time I use this I will start to convert this into a script 🤔😉 For now I am saving this to GitHub in this state so future me could take this in place of extracting from an existing codebase and cutting it to shape.  

Contains:

* Events buses sub stack to centrally export all the sns/eventbridge details for integration with services

* Log bucket

* Dummy Exports for Certificates for US-East-1 (CloudFront etc) and EU-WEST-2 (my preferred region)

* Exports for Route 53 hosted zone for `_DOMAIN_`

* System notification topic, ready destination for CloudWatch alarm notifications

* Events Firehose, Kinesis delivery stream, if you want to define the stream in this stack or in the relevant service is your call, I have not included a kinesis stub in this.  
