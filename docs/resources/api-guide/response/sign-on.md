## Sign On


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
            <td>This Aggregate will return the following.<br> CEUserID : This is the CashEdge internal identifier for a
                user. <br> SessInfo: A security token that can be used to identify a signed-on user.<br></td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the SigonRq</td>
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
        <td>4010</td>
        <td>Error</td>
        <td>Invalid partnerID</td>
        <td>The partnerID specified in the request is invalid.</td>
        <td></td>
    </tr>
    <tr>
        <td>4012</td>
        <td>Error</td>
        <td>Invalid HomeID</td>
        <td>The HomeID specified in the request is invalid.</td>
        <td></td>
    </tr>
    <tr>
        <td>4040</td>
        <td>Error</td>
        <td>User not registered</td>
        <td>The user identified by partnerID:HomeID:UserID is not registered with the &lt;Server&gt;.</td>
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
        <td>Partner should make sure the mandatory parameters are sent in the request and in the defined format as in
            the corresponding XSD.</td>
    </tr>
    <tr>
        <td>4080</td>
        <td>Error</td>
        <td>SessInfo creation failed</td>
        <td>The CashEdge Server was unable to create a SessInfo security token.</td>
        <td>Partner should reinvoke the SingOn API to get the new SessInfo token. If the error continues to occur,
            please reach out to us with the timestamp and CEUserId.</td>
    </tr>
    <tr>
        <td>4090</td>
        <td>Error</td>
        <td>Invalid SessInfo</td>
        <td>The SessInfo token specified in the request is invalid.</td>
        <td>This error occurs when the Session token is invalid or expired; Partner should generate a new SessInfo token
            and reinvoke the process flow with the new SessInfo token. If the error continues to occur, please reach out
            to us with the timestamp and CEUserId.</td>
    </tr>
    <tr>
        <td>4130</td>
        <td>Error</td>
        <td>Invalid role</td>
        <td>A signon has been attempted by a user in a role other than the authorized role.</td>
        <td></td>
    </tr>
    <tr>
        <td>4710</td>
        <td>Error</td>
        <td>User is locked</td>
        <td>The requested user is locked in CashEdge system.</td>
        <td>Partner has to reach out to us with CEUserID.</td>
    </tr>
    <tr>
        <td>7611</td>
        <td>Error</td>
        <td>Request originated from an invalid IP address</td>
        <td>Requested orinigated from unknown (not whitelisted) ip address.</td>
        <td>Partner has to reach out to us to whitelist any new IP's or make the request from whitelisted Ips.</td>
    </tr>
</table>