# Minio Python Library for Amazon S3 Compatible Cloud Storage [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/minio/minio?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Install [![Build Status](https://travis-ci.org/minio/minio-py.svg)](https://travis-ci.org/minio/minio-py)

The recommended technique for installing this package is through pip.

```sh
$ pip install minio
```

## Example

```python
#!/usr/bin/env python

from minio import Minio

# Instantiate a client
client = Minio('https://s3.amazonaws.com',
                access_key='access_key',
                secret_key='secret_key')

# List buckets
buckets = client.list_buckets()
for bucket in buckets:
    print 'bucket:', bucket.name, bucket.creation_date

```

## Examples:

### Bucket Operations.

[make_bucket(bucket)](examples/make_bucket.py)

[list_buckets()](examples/list_buckets.py)

[bucket_exists(bucket)](examples/bucket_exists.py)

[remove_bucket(bucket)](examples/remove_bucket.py)

[get_bucket_acl(bucket)](examples/bucket_acl.py)

[set_bucket_acl(bucketName, acl=Acl.private())](examples/bucket_acl.py)

[list_incomplete_uploads(bucketName, prefix=None, recursive=False)](examples/list_incomplete_uploads.py)

### Object Operations.

[get_object(bucketName, objectName)](examples/get_object.py)

[get_partial_object(bucketName, objectName, offset, length)](examples/get_partial_object.py)

[put_object(bucketName, objectName, length, data, content_type='application/octet_stream')](examples/put_object.py)

[list_objects(bucketName, prefix=None, recursive=False)](examples/list_objects.py)

[stat_object(bucketName, objectName)](examples/stat_object.py)

[remove_object(bucketName, objectName)](examples/remove_object.py)

[remove_incomplete_upload(bucketName, objectName)](examples/remove_incomplete_upload.py)

### Presigned Operations.

[presigned_get_object(bucketName, objectName, expires=604800)](examples/presigned_get_object.py)

[presigned_put_object(bucketName, objectName, expires=604800)](examples/presigned_put_object.py)

[presigned_post_policy(policy=PostPolicy())](examples/presigned_post_policy.py)

## Contribute

[Contributors Guide](./CONTRIBUTING.md)

[![PYPI](https://img.shields.io/pypi/v/minio.svg)](https://pypi.python.org/pypi/minio)
[![PYPI](https://img.shields.io/pypi/l/minio.svg)](https://pypi.python.org/pypi/minio)
[![PYPI](https://img.shields.io/pypi/pyversions/minio.svg)](https://pypi.python.org/pypi/minio)
[![PYPI](https://img.shields.io/pypi/dm/minio.svg)](https://pypi.python.org/pypi/minio)
