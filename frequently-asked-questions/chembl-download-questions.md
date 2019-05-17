# ChEMBL Download Questions

## Is there a file that I can download from the FTP site that contains ALL of the bioactivity data?

No, unfortunately, as there is so much data in ChEMBL, it is not possible to store this on the FTP site as a download. It would be too big to be downloaded to users' computers. If users would like to obtain all of the bioactivity data, we urge them to install a database instance for ChEMBL using Oracle, MySQL, PostgreSQL or SQLite.

## Can I download an SDFile of compounds and associated bioactivity from the interface?

You cannot download a single SDFile of the compound information including the structure, alongside the bioactivity data. However, you can download these separately and use a program such as Pipeline Pilot or Knime to join the files together.

## Is there a password on the MySQL data upload?

No there is no password set for this, so if you are asked for a password it is likely to be a local MS SQL issue and you will need to contact your database administrators to gain access.

## What GB of space is required to upload the data dump files into an Oracle system?

You will need to use a tablespace with about 12GB of free space available to import the ChEMBL oracle dump file.

## What's the difference between the SDFile and the MySQL/Oracle downloads on your FTP server?

The SDfile contains the structures and the IDs of all the compounds currently found in the database. The MySQL/Oracle downloads contain all the compounds and associated bioactivities, but needs to be uploaded into a database to be viewed properly.

## I get an error message when trying to download some data from the interface.

If you get an error message, please send an email to [chembl-help@ebi.ac.uk](mailto:chembl-help@ebi.ac.uk), or create an issue in our [GitHub repository](https://github.com/chembl/GLaDOS). We recommend that you include the full url of the page in your message, this helps us to identify the problem. 

## What is the expiration date in the downloads from the interface?

When a user generates a download from the interface, the file is kept in our servers for 7 days after the file was created. For example, if a file was generated on 17th May 2019 at 8:00 AM, it will be kept in our servers until 24th May 2019 at 8:00 AM. This means that if the same download is requested again during that period, the file will not be generated again and it will be ready to be downloaded immediately. 

During the period in which we keep the downloaded file, we also keep the original query parameters required to generate the file. The parameters and the file itself are deleted after the expiration time has passed.  

