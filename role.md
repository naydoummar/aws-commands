# Create a Role 
## For Lambda
policy-doc.json
```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": "lambda.amazonaws.com"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

`aws iam create-role [--path <value>] --role-name <value> --assume-role-policy-document file://policy-document.json`
`aws iam create-role --path /service-role/ --role-name dxe-slack --assume-role-policy-document file://policy-document.json`
