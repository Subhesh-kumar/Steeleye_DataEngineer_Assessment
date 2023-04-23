#Steeleye_DataEngineer_Assessment
#Python Engineer Assessment

The task involves downloading an XML file from a provided link, parsing it to find the first download link whose file_type is DLTINS
downloading the zip file from that link, and extracting the XML from it. 
Then, the contents of the XML file need to be converted to a CSV file with specific headers, 
namely FinInstrmGnlAttrbts.Id, FinInstrmGnlAttrbts.FullNm, FinInstrmGnlAttrbts.ClssfctnTp, FinInstrmGnlAttrbts.CmmdtyDerivInd, FinInstrmGnlAttrbts.NtnlCcy, and Issr. 
Finally, the resulting CSV file needs to be stored in an AWS S3 bucket.

# The repository contains the solution for SteelEye Python Developer Assignment.
# The solution is written in Python 3 language and requires some additional libraries to be installed.
# The repository consists of the following files:
   * `controller.py`: the main script that calls specific functions from the `helper_functions` module to execute the steps required for the assignment in the correct sequence.
   * `helper_functions.py`: a module that contains all the functions that perform individual steps mentioned in the assignment.
   * `logger.py`: a module that initializes logger which is being used in the `helper_functions` and `controller.py` scripts for logging.
   * `config.cfg`: a configuration file consisting of paths and information required for the script to work.
   * `steel_eye_unittest.py`: a module that performs unit tests.
# The solution uses the following Python modules:
   * os
   * boto3
   * pandas
   * zipfile
   * logging
   * unittest
   * requests
   * xml.etree
   * configparser
# Configuration needs to be done in the `config.cfg` file for the following:
   * `download_path`: the relative path from the current directory of the `controller.py` script where source and target XML files need to be downloaded by the script. The script creates an absolute path during its run.
   * `csv_path`: the relative path from the current directory of the `controller.py` script where the CSV file needs to be created by the script. The script creates an absolute path during its run.
   * `bucket_name`: the name of the S3 bucket to which the file needs to be uploaded.
   * `aws_access_key_id`: the AWS access key ID.
   * `aws_secret_access_key`: the AWS secret access key.
   * `region_name`: the AWS region in which the S3 bucket is hosted.
