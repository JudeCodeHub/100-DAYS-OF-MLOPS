# Day 13 - Pull DVC-Tracked Data from Remote Storage

## Objective

Configure DVC authentication for the remote SeaweedFS storage and successfully retrieve a DVC-tracked dataset into a freshly cloned project.

## Tasks Completed

- Reviewed the existing DVC remote configuration
- Added the required authentication credentials for the SeaweedFS remote
- Verified the remote endpoint and bucket configuration
- Pulled the tracked dataset from the remote DVC storage
- Restored the dataset to the local project directory

## Remote Configuration

- Bucket: `s3://dvc-storage`
- Endpoint: `http://localhost:8333`
- Access Key: `weedadmin`
- Secret Key: `weedadmin123`
- Default Remote: `s3`

## Commands Used

```bash
cd /root/code/fraud-detection/

dvc pull

