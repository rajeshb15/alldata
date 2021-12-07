## Create User


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
            <td>The Status of SignonRs. <br>For StatusCode please refer the signon service</td>
        </tr>
        <tr>
            <td><b>UserAddRs</b></td>
            <td>The user info/profile. <br> </td>
        </tr>
        <tr>
            <td><b>CEUserID</b></td>
            <td> The CashEdge internal identifier for the added user. <br> This element will be present only if the user
                registration is successful. <br></td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the userAdd Request. <br></td>
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
    <tbody>
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
            <td>4012</td>
            <td>Error</td>
            <td>Invalid HomeID</td>
            <td>The HomeID specified in the request is invalid.</td>
            <td></td>
        </tr>
        <tr>
            <td>4030</td>
            <td>Error</td>
            <td>User already registered</td>
            <td>The user identified by partnerID:HomeID:UserID is already registered with the Server.</td>
            <td></td>
        </tr>
        <tr>
            <td>4031</td>
            <td>Error</td>
            <td>Partner client identifier already registered</td>
            <td>test</td>
            <td></td>
        </tr>
        <tr>
            <td>4050</td>
            <td>Error</td>
            <td>Invalid encryption scheme</td>
            <td>The encryption scheme specified in the request is not valid.</td>
            <td></td>
        </tr>
        <tr>
            <td>4070</td>
            <td>Error</td>
            <td>Validation failure</td>
            <td>One or more input fields were not valid.</td>
            <td>Partner should make sure the mandatory parameters are sent in the request and in the defined format as
                in the corresponding XSD.</td>
        </tr>
        <tr>
            <td>4623</td>
            <td>Error</td>
            <td>Day Phone is required</td>
            <td>DayPhone is madatory if the partner home is configured.</td>
            <td></td>
        </tr>
        <tr>
            <td>4626</td>
            <td>Error</td>
            <td>Total phone numbers do not match allowed occurrence</td>
            <td>Telephone numbers provided should not exceed the configured occurance value.</td>
            <td></td>
        </tr>
        <tr>
            <td>4628</td>
            <td>Error</td>
            <td>Invalid Email Address</td>
            <td>E-Mail address provided in the request is invalid</td>
            <td></td>
        </tr>
        <tr>
            <td>4629</td>
            <td>Error</td>
            <td>Only one day phone value is allowed</td>
            <td>DayPhone is provided more than once.</td>
            <td></td>
        </tr>
        <tr>
            <td>4630</td>
            <td>Error</td>
            <td>Only one evening phone value is allowed</td>
            <td>EveningPhone is provided more than once.</td>
            <td></td>
        </tr>
        <tr>
            <td>7621</td>
            <td>Error</td>
            <td>Entitlement parameters are invalid</td>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>