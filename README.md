# Overview

If you are a suitably permissioned company user on ESG Assessment Platform (EAP), you can upload a list of companies to the marketplace which will appear as "pinned" organizations on your Companies page. This specification explains the requirements for creating an uploadable CSV of companies, which may change over time.

Once a file has been validated, it will be uploaded in real-time into EAP and analyzed to ascertain if each company is:

* A reasonably definitive match with an existing organization in EAP, in which case that organization will be automatically pinned, although you will have an opportunity to override that match.
* A possible match with an existing organization in EAP, in which case you will have an opportunity to confirm whether the match is or is not correct
* Not a match with any organization in EAP, in which case the organization will be added on your behalf and then automatically pinned

# Important

Although not all available columns are mandatory, it is <b>strongly recommended</b> that the company data you upload contain as many attributes as possible. Uploading a minimum of attributes will decrease the number of automatic matches against existing organizations in the EAP database, which will decrease the quality of your experience in EAP.

Please take the time to create a robust, attribute-rich dataset before uploading to EAP.

# File Requirements

* Maximum file size is 5MB
* Maximum rows per file is 1,000
* File must have a CSV file extension
* File must have a text MIME type
* Header rows are optional, but if present must match the column names exactly
* Columns must be in the same order as in the "Column Requirements" section

# Column Requirements

<table>
  <tr>
    <td><b>Column</b></td>
    <td><b>Mandatory?</b></td>
    <td><b><b>Format</b></b></td>
    <td><b><b>Max Length</b></b></td>
    <td><b><b>Comments</b></b></td>
  </tr>
  <tr>
    <td>company_name</td>
    <td>Yes</td>
    <td>Text</td>
    <td>100</td>
    <td></td>
  </tr>
  <tr>
    <td>duns</td>
    <td>No</td>
    <td>Numeric</td>
    <td>9</td>
    <td></td>
  </tr>
  <tr>
    <td>lei</td>
    <td>No</td>
    <td>Text</td>
    <td>20</td>
    <td></td>
  </tr>
  <tr>
    <td>website</td>
    <td>Yes</td>
    <td>URL</td>
    <td>100</td>
    <td></td>
  </tr>
  <tr>
    <td>phone</td>
    <td>Yes</td>
    <td>Numeric</td>
    <td>15</td>
    <td>Must only contain integers</td>
  </tr>
  <tr>
    <td>street_address</td>
    <td>Yes</td>
    <td>Text</td>
    <td>100</td>
    <td></td>
  </tr>
  <tr>
    <td>city</td>
    <td>Yes</td>
    <td>Text</td>
    <td>50</td>
    <td></td>
  </tr>
  <tr>
    <td>province_state</td>
    <td>No</td>
    <td>Text</td>
    <td>50</td>
    <td></td>
  </tr>
  <tr>
    <td>country_code</td>
    <td>Yes</td>
    <td>Text</td>
    <td>2</td>
    <td>Must be a <a target='_blank' href='https://esgperformance.sustainalytics.com/country_codes'>valid two-letter ISO country code<a/> </td>
  </tr>
  <tr>
    <td>postal_code</td>
    <td>No</td>
    <td>Text</td>
    <td>10</td>
    <td></td>
  </tr>
  <tr>
    <td>spend_level</td>
    <td>No</td>
    <td>Text</td>
    <td>10</td>
    <td>Must be one of the following values: "low", "medium", "high", "critical"</td>
  </tr>
  <tr>
    <td>employees_total</td>
    <td>No</td>
    <td>Numeric</td>
    <td></td>
    <td>Must be an integer greater than or equal to 0</td>
  </tr>
  <tr>
    <td>annual_sales</td>
    <td>No</td>
    <td>Numeric</td>
    <td></td>
    <td>Value must be in thousands of USD. Must be greater than or equal to 0</td>
  </tr>
  <tr>
    <td>aboriginal_owned</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>aboriginal_led</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>women_owned</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>women_led</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>lgbt_owned</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>lgbt_led</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>veteran_owned</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>veteran_led</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>minority_owned</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>minority_led</td>
    <td>No</td>
    <td>Text</td>
    <td>3</td>
    <td>Must be one of the following values: "Yes" or empty</td>
  </tr>
  <tr>
    <td>external_id</td>
    <td>No</td>
    <td>Text</td>
    <td>20</td>
    <td></td>
  </tr>
</table>

# What Happens When a Company is Uploaded

The uploader first validates that the file is properly formatted. If it finds errors, it reports the first few and asks you to fix the file (and any identical subsequent errors) before re-uploading. If the file is valid, each company is then used to search for a matching company in the database. Where possible matches are found, those matches are presented to the uploading user to confirm. If a company can't be matched, a new company is created. When a new company is created, the company name, location, website, LEI code, etc. are used to create that company in the database. Further, if a pin or tag has been specified, that pin or tag is applied on behalf of the uploading user.

No existing company data is overwritten as part of the uploading process.

# Abuse

Although validation errors are allowed, errors which result from what appear to be deliberate attempts to inject false data or malware into EAP, or to break or compromise EAP in any way, will cause the offending user and company to be banned, and may also result in legal redress.

# Please Contact Us

Although every effort has been made to ensure that this documentation accurately reflects the process for company upload in EAP, please advise us if you discover any discrepancies.
