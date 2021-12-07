## Transactions Categories Info


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
            <td>This Aggregate returns the status of the API request.</td>
        </tr>
        <tr>
            <td><b>SignonRs</b></td>
            <td>The Admin credentials are received as part of this request.</td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the Transcation Categories Info Request.<br />
        </tr>
        <tr>
            <td><b>CategoryRec</b></td>
            <td>This Aggregate will return the Category Name and ID for transactions.</td>
        </tr>
        <tr>
            <td><b>Name</b></td>
            <td>This Aggregate will return the Category Name for transaction
        </tr>
        <tr>
            <td><b>Id<b></td>
            <td> This Aggregate will return the Category Id for transaction <br> This element will be present only if
                the user registration is successful. <br />
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the TransCategoriesInfoRq</td>
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
        <td>There was an error that prevented the service provider from processing the transaction. No additional
            information is provided.</td>
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
        <td>4060</td>
        <td>Info</td>
        <td>No data available</td>
        <td>No data is available to satisfy the request. This could mean that the user has not registered any financial
            institutions; there are no transactions in the specified date range and so on.</td>
        <td>If this error occurs on invoking getAccountDetails API, it means user has not added any financial
            institutions. Please make sure user has added accounts successfully under any financial institutions. If
            this error occurs on invoking transactions APIs, make sure the 'LastSuccessfulUpdate' date is returned in
            getAccountDetails API for that specific account and the specified date range lies within the
            'LastSuccessfulUpdate' date.</td>
    </tr>
</table>