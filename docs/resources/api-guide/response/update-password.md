## Update Password


<b>Response Code 200</b>

<table>
    <thead>
        <th>Element/property</th>
        <th>Description</th>
    </thead>
    <tbody>
        <tr>
            <td><b>RqUID</b></td>
            <td>A Unique Request Identifier.</td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the request.</td>
        </tr>
    </tbody>
</table>

<b>See Possible Status Codes below</b>

<table>
    <thead>
        <tr></tr>
        <th>StatusCode</th>
        <th>Severity</th>
        <th>StatusDesc</th>
        <th>Condition</th>
        <th>Action API Partner should take to resolve the error</th>
        </tr>
    </thead>
    <tr>
        <td>4070</td>
        <td>Error</td>
        <td>Validation failure</td>
        <td>One or more input fields were not valid.</td>
        <td>Partner should make sure the mandatory parameters are sent in the request and in the defined format as in
            the corresponding XSD.</td>
    </tr>
    <tr>
        <td>100</td>
        <td>Error</td>
        <td>General Error</td>
        <td>There was an error that prevented the service provider from processing the transaction. No additional
            information is provided.</td>
        <td>If this error continues to occur, please reach out to us the timestamp and CEUserId.</td>
    </tr>
    <tr>
        <td>0</td>
        <td>Info</td>
        <td>Success</td>
        <td>The service provider successfully processed the request.</td>
        <td></td>
    </tr>
</table>