<center><a href='https://theomx.com'><img src="https://theomx.com/assets/new/omx_logo-e309ca445f44378e718aa40cd5c054c14d18337b4706f912ec3ec47935432af1.png" width="200" ></a></center>

# Overview

If you are a suitably permissioned company user on OMX, you can upload a list of companies to the marketplace which will appear as "pinned" organizations on your Companies page. This specification explains the requirements for creating an uploadable CSV of companies, which may change over time.

Once a file has been validated, it will be uploaded in real-time into OMX and analyzed to ascertain if each company is:

* A reasonably definitive match with an existing organization in OMX, in which case that organization will be automatically pinned, although you will have an opportunity to override that match.
* A possible match with an existing organization in OMX, in which case you will have an opportunity to confirm whether the match is or is not correct
* Not a match with any organization in OMX, in which case the organization will be added on your behalf and then automatically pinned

# Important

Although not all available columns are mandatory, it is <b>strongly recommended</b> that the company data you upload contain as many attributes as possible. Uploading a minimum of attributes will decrease the number of automatic matches against existing organizations in the OMX database, which will decrease the quality of your experience in OMX.

Please take the time to create a robust, attribute-rich dataset before uploading to OMX.

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
    <td>cage</td>
    <td>No</td>
    <td>Text</td>
    <td>5</td>
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
    <td>Text</td>
    <td>15</td>
    <td></td>
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
    <td>Must be a <a target='_blank' href='https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes'>valid two-letter ISO country code<a/> </td>
  </tr>
  <tr>
    <td>postal_code</td>
    <td>Yes</td>
    <td>Text</td>
    <td>10</td>
    <td></td>
  </tr>
</table>

# Abuse

Although validation errors are allowed, errors which result from what appear to be deliberate attempts to inject false data or malware into OMX, or to break or compromise OMX in any way, will cause the offending user and company to be banned, and may also result in legal redress.

# Please Contact Us

Although every effort has been made to ensure that this documentation accurately reflects the process for company upload in OMX, please advise us if you discover any discrepancies.
