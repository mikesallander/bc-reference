## CaseList_EntityRetrieve

Retrieves a list of cases for a given entity.

### Request

* **Method:** SOAP
* **Server:** worldsecuresystems.com
* **Path:** /catalystwebservice/catalystcrmwebservice.asmx
* **Auth:** Username/password or a site token can be used (example below uses site token)

#### Parameters

* `siteId` - ID of the site *(integer)*
* `username` - email address of user account, leave empty if using site token *(string)*
* `password` - password of user account, or site authentication token for specified site *(string)*
* `entityId` - *(integer)*
* `recordStart` - *(integer)*
* `moreRecords`  - *(boolean)*

To use a site token instead of username/password, send an empty `username` field and the site token as the `password`. See example below.

### Response

A CaseList_EntityRetrieveResponse object with the following properties:

* `CaseList_EntityRetrieveResult` *(object)*
    * `CaseDetails` *(object)*
        * `entityId` - *(integer)*
        * `caseId` -  *(integer)*
        * `assignedTo` - *(integer)*
        * `caseSubject` - *(string)*
        * `createDate`- *(dateTime)*
        * `lastUpdateDate`- *(dateTime)*
        * `messageThreads`- *(array)*
        * `crmForms` - *(array)*
        * `fileList` - *(array)*


### Examples

Accepts and returns XML as Content-Type. 

The following is a sample SOAP 1.2 request and response. The placeholders shown need to be replaced with actual values.

**Request:**
~~~
POST /catalystwebservice/catalystcrmwebservice.asmx HTTP/1.1
Host: worldsecuresystems.com
Content-Type: application/soap+xml; charset=utf-8
Content-Length: length

<?xml version="1.0" encoding="utf-8"?>
<soap12:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap12="http://www.w3.org/2003/05/soap-envelope">
  <soap12:Body>
    <CaseList_EntityRetrieve xmlns="http://tempuri.org/CatalystDeveloperService/CatalystCRMWebservice">
      <username>string</username>
      <password>string</password>
      <siteId>int</siteId>
      <entityId>int</entityId>
      <recordStart>int</recordStart>
      <moreRecords>boolean</moreRecords>
    </CaseList_EntityRetrieve>
  </soap12:Body>
</soap12:Envelope>
~~~

**Response:**
~~~
HTTP/1.1 200 OK
Content-Type: application/soap+xml; charset=utf-8
Content-Length: length

<?xml version="1.0" encoding="utf-8"?>
<soap12:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap12="http://www.w3.org/2003/05/soap-envelope">
  <soap12:Body>
    <CaseList_EntityRetrieveResponse xmlns="http://tempuri.org/CatalystDeveloperService/CatalystCRMWebservice">
      <CaseList_EntityRetrieveResult>
        <CaseDetails>
          <entityId>int</entityId>
          <caseId>int</caseId>
          <assignedTo>int</assignedTo>
          <caseSubject>string</caseSubject>
          <createDate>dateTime</createDate>
          <lastUpdateDate>dateTime</lastUpdateDate>
          <messageThreads>
            <MessageThreads xsi:nil="true" />
            <MessageThreads xsi:nil="true" />
          </messageThreads>
          <crmForms>
            <CrmForms xsi:nil="true" />
            <CrmForms xsi:nil="true" />
          </crmForms>
          <fileList>
            <Files xsi:nil="true" />
            <Files xsi:nil="true" />
          </fileList>
        </CaseDetails>
        <CaseDetails>
          <entityId>int</entityId>
          <caseId>int</caseId>
          <assignedTo>int</assignedTo>
          <caseSubject>string</caseSubject>
          <createDate>dateTime</createDate>
          <lastUpdateDate>dateTime</lastUpdateDate>
          <messageThreads>
            <MessageThreads xsi:nil="true" />
            <MessageThreads xsi:nil="true" />
          </messageThreads>
          <crmForms>
            <CrmForms xsi:nil="true" />
            <CrmForms xsi:nil="true" />
          </crmForms>
          <fileList>
            <Files xsi:nil="true" />
            <Files xsi:nil="true" />
          </fileList>
        </CaseDetails>
      </CaseList_EntityRetrieveResult>
      <recordStart>int</recordStart>
      <moreRecords>boolean</moreRecords>
    </CaseList_EntityRetrieveResponse>
  </soap12:Body>
</soap12:Envelope>
~~~
