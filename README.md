# Configure AWS access using cli

1. Create access keys in aws portal -> security credentials -> create access key
2. Install aws cli: `sudo snap install aws-cli --classic`
3. In cli run `aws configure` and enter access key, secret access key and region

# IAC

I am using terraform to create the EKS cluster that will run the workloads.  
The terraform files are in the `infra` folder.

# The docker image

The docker image itself runs rootless, and is based on python alpine which gives it a smaller size and a faster build time.

To run the image using docker (for testing purposes), execute the following command:
```bash
docker run -it --rm -e PORT=<port-number> -p <port-number>:<port-number> <image-name>
```