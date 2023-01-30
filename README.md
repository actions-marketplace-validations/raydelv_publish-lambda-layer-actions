# GitHub Action - AWS Lambda Layer Publish

Docs from AWS Lambda JS SDK: https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/Lambda.html#publishLayerVersion-property.

Run PublishLayerVersion.

## Secret

Add Secret before this action. `Settings > Secrets > Add a new secret`

- `AWS_REGION`
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`

## Example
```yml
- name: Publish AWS Lambda Layer w/Version
  uses: raydelv/publish-lambda-layer-actions@aws_lambda
  env:
    AWS_REGION: ${{ secrets.AWS_REGION }}
    AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
    AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
  with:
    layer_name: TargetFunctionName
    zip_file: path/to/file.zip
    compatible_runtimes: runtimes
```
