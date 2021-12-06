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
            <td>TheAdmin credentials are received as part of this request.</td>
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
            <td>
                The status of the TransCategoriesInfoRq
                <br>
                <br>
                <table>
                    <tr>
                        <td><b>StatusCode</b></td>
                        <td><b>StatusDesc</b></td>
                    </tr>
                    <tr>
                        <td>0</td>
                        <td>Success</td>
                    </tr>
                    <tr>
                        <td>100</td>
                        <td>General Error</td>
                    </tr>
                    <tr>
                        <td>1740</td>
                        <td>Authentication Failed</td>
                    </tr>
                    <tr>
                        <td>4060</td>
                        <td>No data available</td>
                    </tr>
                </table>
            </td>
        </tr>
    </tbody>
</table>