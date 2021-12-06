## Search Financial Institution


<b>Response Code 200</b>

<table>
    <thead>
        <th>Element / property</th>
        <th>Description</th>
    </thead>
    <tbody>
        <tr>
            <td><b>RqUID</b></td>
            <td>Unique Request Identifier. The ClientSite sends this element with the request.</td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>The status of the request.</td>
        </tr>
        <tr>
            <td><b>FIInfoDataList</b></td>
            <td>Listof FI along with their requisite information.<br>This aggregate willbe present, only if the request was carried out successfully and thisoption was desired in the request.</td>
        </tr>
        <tr>
            <td><b>FIIdList</b></td>
            <td>Listof FI id’s.<br>This aggregate will be present, only if the request was carried out successfully and this option was desired in the request.</td>
        </tr>
        <tr>
            <td><b>Status</b></td>
            <td>
                The status of the FISearchRs
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
                    <tr>
                    <tr>
                        <td>100</td>
                        <td>General Error</td>
                    <tr>
                    <tr>
                        <td>4060</td>
                        <td>No Data Available</td>
                    <tr>
                    <tr>
                        <td>4070</td>
                        <td>Invalid data in request</td>
                    <tr>
                    <tr>
                        <td>4360</td>
                        <td>Data insufficient to carry out request</td>
                    <tr>
                    <tr>
                        <td>4591</td>
                        <td>No FIs found matching the search criteria provided</td>
                    <tr>
                </table>
            </td>
        </tr>
    </tbody>
</table>