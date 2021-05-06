============
VIDEO FILES DOWNLOADER/UPLOADER
============

A Python3 multiple video files dowloader/uploader specifically made for use with Drupal 8/9 content interface. It can download/upload multiple type file extensions, i.e., PDF, DOCX, DOC, TXT, WRF, XLS, XLSX, BZ2, TAR, TAR.GZ and more.

Features:

- Uploads multiple documents to Drupal 8/9 user interface.
- Downloads multiple documents from any website.
- Does not need any monitoring, will happily upload/download all downloadable documents.
- Can upload hundreds, even thousands (theoretically), of documents stored in its predefined directory.

Contributions and comments are welcome at:
http://github.com/jbernadas/document-uploader

All you need to run this CLI app is VirtualEnv (https://pypi.org/project/virtualenv/). VirtualEnv lets you run your Python script inside a virtual environment, isolated from all other modules. Using virtualenv you can let pip manage your dependencies automatically. However, if you would rather not use VirtualEnv, you can download the following dependencies one-by-one:

- selenium
- os
- lxml
- bs4
- requests
- urllib

IMPORTANT: Whether you are using virtualenv or not you need to have GeckoDriver installed, it is a Mozilla product used for automated testing, it is required when using the upload function of this app. Install it manually then make sure it is in your computer's PATH environment.

- geckodriver - downloaded separately from Mozilla repository at https://github.com/mozilla/geckodriver

Installation
============

1. Inside your terminal, clone as usual:
::
  git clone https://github.com/jbernadas/video-file-downloader-uploader

2. CD into the newly created directory:
::
  cd vide-file-dowloader-uploader

3. Assuming you have already installed virtualenv, you can now create a virtual environment folder called venv inside the root folder:
::
  python3 -m venv venv

4. Fireup your virtualenv (Linux/Mac):
::
  source venv/bin/activate

or fireup your virtualenv (Windows):
::
  venv\Scripts\activate

5. Automatically install all of our projects dependencies by issuing the following command:
::
  pip install -r requirements.txt

6. For usage see below.

7. Finally, once you are done using this CLI app, deactivate your virtual environment by issuing the below command:
::
  deactivate

Configuration
=============

None.

Documentation
=============

You can tweak the arguments and parameters to make it find the necessary targets.

Usage
=====

Downloading
***********

1. cd into the root directory:
::
  cd downloader-uploader

2. Before you begin, you can pick which file extensions the downloader will dowload by commenting or commenting-out the arrays iside the QUALIFIERS array of downloader-uploader.py.

3. Once you are ready, issue the below command to begin:
::
  python3 downloader-uploader.py

4. The script will ask you if you want to Download or Upload documents. Choose 'd' for download.
5. The script will ask the URL that we are downloading from, i.e., https://google.com
6. Wait for the script to download all the files into the docs_for_upload directory.
7. Once you're done downloading, don't forget to turn off your Python virtual environment:
::
  deactivate

Uploading
*********

1. Make sure all the documents you want to upload are inside the docs_for_upload folder.

2. Fire up the script by the below command:
::
  python3 downloader-uploader.py

3. The script will ask you if you want to Download or Upload documents. Choose 'u' for upload.
4. The script will ask the URL that we are uploading to, i.e., https://google.com
5. Once the script has opened a new browser it will wait for you to login to your Drupal site, and ask if you are ready to proceed. Hit 'y' for yes, 'a' for abort.
6. The script will now automatically upload each document inside the docs_for_upload folder one by one.
7. Once you're done uploading, don't forget to deactivate your Python virtual environment:
::
  deactivate


Bugs & Contribution
===================

Please use Github to report bugs, feature requests and submit your code:
http://github.com/jbernadas/document-uploader

:author: Joseph Bernadas
:version: 0.1.0
:date: 2020/06/26
:license: GPL version 3
