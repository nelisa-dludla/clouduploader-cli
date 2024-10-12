# CloudUploader CLI

CloudUploader is a simple command-line tool that allows users to upload files to a specified Google Cloud Storage bucket. This tool is designed to help users manage their cloud storage files easily from the command line.

## Overview

CloudUploader utilizes the Google Cloud SDK (`gcloud`) to facilitate file uploads. Users can specify a file to upload and an optional bucket name. If no bucket name is provided, it defaults to `"gcp-file-storage"`.

## Prerequisites

Before using CloudUploader, ensure you have the following:

1. **Google Cloud SDK**: Make sure the Google Cloud SDK is installed on your machine. You can download and install it from [Google Cloud SDK Installation](https://cloud.google.com/sdk/docs/install).

2. **Authenticated Account**: You must authenticate your account using the following command:
   ```bash
   gcloud auth login
   ```

3.  **Billing Enabled**: Ensure that billing is enabled for your Google Cloud project where the bucket resides.
    
4.  **Permissions**: You should have the necessary permissions to upload files to the specified Cloud Storage bucket.
    

## Setup

1.  **Clone the Repository**:
	```bash
	git clone https://github.com/yourusername/clouduploader.git
	cd clouduploader
	```
	
2. **Make the Script Executable**:
	```bash
	chmod +x clouduploader.sh
	```

3. **Run the Script**: You can run the script by using the following command:
	```bash
	./clouduploader.sh /path/to/file.txt [bucket-name]```

## Usage Examples

-   To upload a file to the default bucket:
	```bash
	./clouduploader.sh /path/to/file.txt```
- To upload a file to a specific bucket:
	```bash
	./clouduploader.sh /path/to/file.txt my-custom-bucket
	```
## Troubleshooting

If you encounter issues while using CloudUploader, consider the following troubleshooting tips:

1.  **Check Bucket Name**: Ensure that the bucket name is correct and exists in your Google Cloud account.
    
2.  **Permissions Issue**: If you receive permission errors, verify that your Google Cloud account has the required permissions to upload files to the specified bucket.
    
3.  **Billing Issues**: If you see errors related to billing, ensure that your billing account is active and linked to the project.
    
4.  **gcloud Not Found**: If you receive an error stating that `gcloud` is not found, make sure you have installed the Google Cloud SDK and that it's added to your system's PATH.
    
5.  **File Not Found**: If you receive an error indicating that the specified file does not exist, double-check the file path you provided.
    
6.  **Enable Debugging**: You can enable debugging by adding `set -x` at the top of the script to get detailed output on what the script is doing.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE.md) file for details.
