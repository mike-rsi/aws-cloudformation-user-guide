# AWS::CloudFormation::WaitConditionHandle<a name="aws-properties-waitconditionhandle"></a>

**Important**  
For Amazon EC2 and Auto Scaling resources, we recommend that you use a CreationPolicy attribute instead of wait conditions\. Add a CreationPolicy attribute to those resources, and use the cfn\-signal helper script to signal when an instance creation process has completed successfully\.  
For more information, see [Deploying Applications on Amazon EC2 with AWS CloudFormation](deploying.applications.md)\.

The AWS::CloudFormation::WaitConditionHandle type has no properties\. When you reference the WaitConditionHandle resource by using the `Ref` function, AWS CloudFormation returns a presigned URL\. You pass this URL to applications or scripts that are running on your Amazon EC2 instances to send signals to that URL\. An associated [AWS::CloudFormation::WaitCondition](aws-properties-waitcondition.md) resource checks the URL for the required number of success signals or for a failure signal\.

**Important**  
Anytime you add a `WaitCondition` resource during a stack update or update a resource with a wait condition, you must associate the wait condition with a new `WaitConditionHandle` resource\. Do not reuse an old wait condition handle that has already been defined in the template\. If you reuse a wait condition handle, the wait condition might evaluate old signals from a previous create or update stack command\.

**Note**  
Updates are not supported for this resource\.

## Syntax<a name="aws-resource-cloudformation-waitconditionhandle-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-waitconditionhandle-syntax.json"></a>

```
{
   "Type" : "AWS::CloudFormation::WaitConditionHandle",
   "Properties" : {
   }
}
```

### YAML<a name="aws-resource-cloudformation-waitconditionhandle-syntax.yaml"></a>

```
Type: "AWS::CloudFormation::WaitConditionHandle"
Properties:
```

## Related Resources<a name="w3ab2c21c10d210c13"></a>

For information about how to use wait conditions, see [Creating Wait Conditions in a Template](using-cfn-waitcondition.md)\.