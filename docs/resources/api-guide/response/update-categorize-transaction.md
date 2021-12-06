## Categorize Transaction


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
            <td>The status of the Transscation Categories Info Request.<br></td>
        </tr>
        <tr>
            <td><b>TransID</b></td>
            <td>Unique Transaction Identifier. <br> </td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the UpdateTxnCategoryRq</td>
        </tr>
        <tr>
            <td></td>
            <td><span>Possible Status Code</span><br><br>
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
                        <td>4060</td>
                        <td>Info</td>
                        <td>No data available</td>
                        <td>No data is available to satisfy the request. This could mean that the user has not registered any financial institutions; there are no transactions in the specified date range and so on.</td>
                        <td>If this error occurs on invoking getAccountDetails API, it means user has not added any financial institutions. Please make sure user has added accounts successfully under any financial institutions. If this error occurs on invoking transactions APIs, make sure the 'LastSuccessfulUpdate' date is returned in getAccountDetails API for that specific account and the specified date range lies within the 'LastSuccessfulUpdate' date.</td>
                    </tr>
                    <tr>
                        <td>4070</td>
                        <td>Error</td>
                        <td>Validation failure</td>
                        <td>One or more input fields were not valid.</td>
                        <td>Partner should make sure the mandatory parameters are sent in the request and in the defined format as in the corresponding XSD.</td>
                    </tr>
                    <tr>
                        <td>4100</td>
                        <td>Error</td>
                        <td>Invalid FIAcctId</td>
                        <td>The FIAcctId specified in the request is invalid.</td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>4110</td>
                        <td>Error</td>
                        <td>AcctType mismatch</td>
                        <td>The account specified in the request is not of the type specified in the request.</td>
                        <td>Partner can verify AcctType of the accounts from getAccountDetails API response.</td>
                    </tr>
                    <tr>
                        <td>4120</td>
                        <td>Error</td>
                        <td>Not owner</td>
                        <td>The FILogin Account or FI Account for which a user is requesting details does not belong to the user.</td>
                        <td>This error occurs when FILoginAcctId or AcctId sent by Partner doesnot exist in our system or the Id's belong to a different CEUserID in the system.</td>
                    </tr>
                    <tr>
                        <td>4150</td>
                        <td>Error</td>
                        <td>Invalid AcctType</td>
                        <td>The AcctType or ExtAcctType specified in the request are invalid.</td>
                        <td>Partner can verify AcctType or ExtAcctType of the accounts from getAccountDetails API response.</td>
                    </tr>
                    <tr>
                        <td>7601</td>
                        <td>Error</td>
                        <td>Validation failure</td>
                        <td>Transaction Not Found.</td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>7602</td>
                        <td>Error</td>
                        <td>Validation failure</td>
                        <td>Category Not Found.</td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>7603</td>
                        <td>Error</td>
                        <td>Validation failure</td>
                        <td>SubCategory Not Found.</td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>7604</td>
                        <td>Error</td>
                        <td>Validation failure</td>
                        <td>Subcategory already exists.</td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>7610</td>
                        <td>Error</td>
                        <td>Validation failure</td>
                        <td>Invalid account Type.</td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>7611</td>
                        <td>Error</td>
                        <td>Request originated from an invalid IP address</td>
                        <td>Requested orinigated from unknown (not whitelisted) ip address.</td>
                        <td>Partner has to reach out to us to whitelist any new IP's or make the request from whitelisted IPs.</td>
                    </tr>
                </table>
            </td>
        </tr>
    </tbody>
</table>