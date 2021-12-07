## Delete Subcategory


<b>Response Code 200</b>

<table>
    <thead>
        <th>Element / property</th>
        <th>Description</th>
    </thead>
    <tbody>
        <tr>
            <td><b>RqUID</b></td>
            <td>A Unique Request Identifier.</td>
        </tr>
        <tr>
            <td><b>Status </b></td>
            <td>This Aggregate returns the status of the API.</td>
        </tr>
        <tr>
            <td><b>SignonRs</b></td>
            <td>This aggregate provides the status of the user authentication status.</td>
        </tr>
        <tr>
            <td><b>StatusCode</b></td>
            <td>The status code for the response.A code of “0” implies complete success.Other status codes could mean
                either success or failure depending upon the value of the severity of the code.</td>
        </tr>
        <tr>
            <td><b>Severity</b></td>
            <td>Conveys the status of the request, whether the request was processed successfully, or whether some error
                was encountered while processing the request.</td>
        </tr>
        <tr>
            <td><b>StatusDesc</b></td>
            <td>A meaningful message that conveys the nature of the error, if any.</td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the DeleteSubCategoryRq</td>
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
    </thead>
    <tr>
        <td>0</td>
        <td>Info</td>
        <td>Success</td>
        <td>The service provider successfully processed the request.</td>
        <td></td>
    </tr>
    <tr>
        <td>100</td>
        <td>Error</td>
        <td>General Error</td>
        <td>There was an error that prevented the service provider from processing the transaction. No additional information is provided.</td>
        <td>If this error continues to occur, please reach out to us the timestamp and CEUserId.</td>
    </tr>
    <tr>
        <td>1740</td>
        <td>Error</td>
        <td>Authentication Failed</td>
        <td>The customer could not be authenticated due to an incorrect HomeID, login ID or password.</td>
        <td>Verify the user Login ID and Password</td>
    </tr>
    <tr>
        <td>4012</td>
        <td>Error</td>
        <td>Invalid HomeID</td>
        <td>The HomeID specified in the request is invalid.</td>
        <td></td>
    </tr>
    <tr>
        <td>4070</td>
        <td>Error</td>
        <td>Validation failure</td>
        <td>One or more input fields were not valid.</td>
        <td>Partner should make sure the mandatory parameters are sent in the request and in the defined format as in the corresponding XSD.</td>
    </tr>
    <tr>
        <td>4130</td>
        <td>Error</td>
        <td>Invalid role</td>
        <td>A signon has been attempted by a user in a role other than the authorized role.</td>
        <td></td>
    </tr>
    <tr>
        <td>7603</td>
        <td>Error</td>
        <td>Validation failure</td>
        <td>SubCategory Not Found.</td>
        <td></td>
    </tr>
</table>