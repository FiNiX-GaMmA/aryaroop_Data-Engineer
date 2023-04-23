# SteelEye Python Engineer Assessment Test

This is my solution to the Python Engineer Assessment Test for SteelEye. The goal of this test is to download an XML file from a given link, extract a zip file from it, convert the contents of the XML file into a CSV with specific headers, and store the CSV file in an AWS S3 bucket. 

## Requirements

The requirements for this solution are as follows:

- The code should be developed in Python 3.
- The code should follow PEP8 standards and should include pydoc, logging, and unit tests.
- The code should download the XML file from a given link.
- From the XML file, the code should parse through to the first download link whose file_type is DLTINS and download the zip file.
- The code should extract the XML file from the zip file.
- The code should convert the contents of the XML file into a CSV file with specific headers.
- The CSV file should be stored in an AWS S3 bucket.
- The above function should be run as an AWS Lambda (optional).

## Solution Overview

The solution consists of the following steps:

1. Download the XML file from the given link.
2. Parse through the XML file to find the first download link whose file_type is DLTINS.
3. Download the zip file from the download link.
4. Extract the XML file from the zip file.
5. Convert the contents of the XML file into a CSV file with specific headers.
6. Store the CSV file in an AWS S3 bucket.

## Code Structure

The solution is implemented in the form of a Python module named `solution`. It consists of the following files:
- `get_download_link` : Parses the given XML file(reponse.xml) and returns the first download link found in it.
- `download_file`: Download a file from the given URL and save it to the specified filename.
- `get_file_size`: Get the size of a file in MB.
- `extract_zip_file`: A function to extract the XML file from the downloaded zip file.
- `remove_xml_namespace`: Fucntion to remove all namespaces from an XML file.
- `s3_operations`: Perform S3 operations including creating a bucket, uploading a file.

## Dependencies

The solution depends on the following Python packages:

- `boto3`: A Python library for AWS services.
- `requests`: A Python library for HTTP requests.
- `xml.etree.ElementTree` - A Python library for processing the XML file.
- `zipfile` - A Python library for extracting or zipping files

## Testing

The solution has been thoroughly tested with unit tests. The tests cover all the functions in the solution and ensure that they are working correctly. The tests also check that the CSV file has the correct headers and that it has been uploaded to the S3 bucket. The tests are run using the `unittest` module.

## Conclusion

This solution satisfies all the requirements specified in the Python Engineer Assessment Test. It follows PEP8 standards, includes pydoc, logging, and unit tests, and has good code coverage. The solution is simple, efficient, easy to maintain, and easy for the user to use.
