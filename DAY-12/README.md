# Day 12 - Configure DVC Remote and Push Data to SeaweedFS

## Objective

Configure a DVC remote storage backend and push versioned dataset files from the local repository to a shared S3-compatible object store (SeaweedFS).

## Tasks Completed

- Reviewed and corrected `.dvc/config` remote configuration
- Fixed incorrect S3 bucket reference
- Corrected SeaweedFS endpoint URL
- Ensured access credentials for remote storage are properly set
- Set the `s3` remote as the default DVC remote
- Pushed DVC-tracked dataset to SeaweedFS object storage

## Remote Configuration Fixed

- Bucket: `s3://dvc-storage`
- Endpoint: `http://localhost:8333`
- Credentials:
  - access_key_id: `weedadmin`
  - secret_access_key: `weedadmin123`
- Default remote: `s3`

## Commands Used

```bash
cd /root/code/fraud-detection/

dvc remote modify s3 url s3://dvc-storage
dvc remote modify s3 endpointurl http://localhost:8333

dvc remote default s3

dvc push