# animated-random-user-picker

Visit http://animated-random-user-picker.s3-website-ap-northeast-1.amazonaws.com/

All example image copyrights belongs to www.irasutoya.com

## how to deploy on S3

- change images under `img` directory
- rewrite image paths in `index.html`
- run commands below

```
aws s3 mb s3://animated-random-user-picker # only once
aws s3 website s3://animated-random-user-picker --index-document index.html # only once
aws s3api put-bucket-policy --bucket animated-random-user-picker --policy file://policy.json # only once
aws s3 sync . s3://animated-random-user-picker
```
