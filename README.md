# JCDatatable
JCDatatable is a adaptation of Javascript Datatables inside Salesforce. With this component you could:

  - Pretty tables
  - Pagination
  - Instant search and multi-column
  - Page Sizes and default page size on load.


### Version
Beta 0.1

<a href="https://githubsfdeploy.herokuapp.com?owner=Juanpe&repo=JCDatatable">
  <img alt="Deploy to Salesforce"
       src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/src/main/webapp/resources/img/deploy.png">
</a>

<img alt="Deploy to Salesforce" src="http://juanpecatalan.com/jcdatatable.png">

### Sample Usage PageBlockTable

```bash
<apex:pageBlock title="PageBlockTable">

    <apex:pageBlockTable value="{!accounts}" var="acc" id="pageBlockTable">
        <apex:column value="{!acc.AccountNumber}"/>
        <apex:column value="{!acc.Name}"/>
        <apex:column value="{!acc.Industry}"/>
        <apex:column value="{!acc.NumberOfEmployees}"/>
        <apex:column value="{!acc.Website}"/>
        <apex:column value="{!acc.Owner.Name}"/>
    </apex:pageBlockTable>

    <c:JCDatatable tableID="pageBlockTable" EmptyMsg="No hay datos"/>

</apex:pageBlock>
```

### Sample Usage DataTable

```bash
<apex:pageBlock title="dataTable">
    <apex:dataTable value="{!accounts}" var="acc" id="dataTable">
        <apex:column headerValue="Account Number">              
            <apex:outputLink value="/{!acc.Id}" id="theLink1">{!acc.AccountNumber}</apex:outputLink>
        </apex:column>
        <apex:column headerValue="Name">
            <apex:outputLink value="/{!acc.Id}" id="theLink3">{!acc.Name}</apex:outputLink>
        </apex:column>
        <apex:column headerValue="Industry">
            {!acc.Industry}
        </apex:column>          
        <apex:column headerValue="Employees">
            {!acc.NumberOfEmployees}
        </apex:column>
        <apex:column headerValue="Website">
            {!acc.Website}
        </apex:column>
        <apex:column headerValue="Owner">
            <apex:outputLink value="/{!acc.Owner.Id}" id="theLink5">{!acc.Owner.Name}</apex:outputLink>
        </apex:column>
    </apex:dataTable>

    <c:JCDatatable tableID="dataTable" EmptyMsg="No hay datos"/>

</apex:pageBlock>
```

### Todo's

 - Fully internationalisable
 - Responsive
 - Alternative themes
 - Export to CSV and PDF, copy to clipboard and print


