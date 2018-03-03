def lambda_handler(event, context):
    # TODO implement
    import boto3
    print 'start execution'
    cf_client = boto3.client('cloudformation')
    Capabilities=['CAPABILITY_IAM']
    cf_client.create_stack(
    StackName='VPC-30',
    Capabilities=['CAPABILITY_IAM'],
    TemplateURL='https://s3.amazonaws.com/onetouchproject/VPCwithEC2andIAM.yaml'
    )