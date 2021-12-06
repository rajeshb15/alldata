## Financial Institution Info


<b>Response 200</b>

<table>
    <thead>
        <th>Element / property</th>
        <th>Description</th>
    </thead>
    <tbody>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the request.</td>
        </tr>
        <tr>
            <td><b>RqUID</b></td>
            <td> Unique Request Identifier. The Client Site sends this element with the request.</td>
        </tr>
        <tr>
            <td><b>FIInfoDataList</b></td>
            <td> List of FI along with their requisite information.<br>This aggregate will be present, only if the
                request was carried out successfully and this option was desired in the
                request. </td>
        </tr>
        <tr>
            <td><b>FIIdList</b></td>
            <td> List of FI id’s.<br>This aggregate will be present, only if the request was carried out successfully
                and this option was desired in the request.</td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>
                The status of the FIInfoRs <br><br>
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
                        <td>4060</td>
                        <td>No data available</td>
                    </tr>
                    <tr>
                        <td>4070</td>
                        <td>Invalid data in request</td>
                    </tr>
                    <tr>
                        <td>4260</td>
                        <td>Invalid Date</td>
                    </tr>
                    <tr>
                        <td>9001</td>
                        <td>Support for this ABA routing number coming soon.</td>
                    </tr>
                    <tr>
                        <td>9002</td>
                        <td>ABA number is not supported.</td>
                    </tr>
                </table>
            </td>
        </tr>
    </tbody>
</table>