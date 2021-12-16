# User Management Web Services

This chapter lists each User Management API in a table with a resource URL, descriptive information, and a link to Swagger documentation.

## createUser
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>createUser</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/UserMgmt/createUser</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                <li>This API is used to add/register the user with the AllData system.</li>
                <li>Minimum information required to register a user is username and password.</li>
                <li>Username must be unique within Home and cannot be changed.</li>
                <li>Username can be a maximum of 32 characters in length.</li>
                <li>Username can be alphanumeric but does not allow special characters except underscore.</li>
                <li>These reserved words are forbidden in usernames: admin, Fiserv, administrator, user</li>
                <li>Password must be at least 8 characters and no more than 64 characters long.</li>
                <li>Password is case-sensitive.</li>
                <li>Password should not contain any spaces.</li>
                <li>Password should not contain non-printable characters such as space or tab.</li>
                <li>Returns numeric CEUserID if user is successfully created (useful for debugging issues)</li><br>
                <b>Note:</b> Users with &quot;Admin&quot; role cannot be added using this API; the AllData Professional Services team creates admin users during implementation. |
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/User%20Management%20Service/createUser">createUser API docs</a>
            </td>
        </tr>
    </tbody>
</table>

## deleteUser
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>deleteUser</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/UserMgmt/deleteUser</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                <li>This API is used to unregister a previously registered user.</li>
                <li>User data including accounts, transactions, etc., are deleted.</li>
                <li>Admin users cannot be deleted using this service.</li>
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/User%20Management%20Service/deleteUser">deleteUser API docs</a>
            </td>
        </tr>
    </tbody>
</table>

## getUserProfile
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>getUserProfile</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/UserMgmt/getUserProfile</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                <li>This API is used to retrieve user profile information such as name, address, and contact details.</li>
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/User%20Management%20Service/getUserProfile">getUserProfile API docs</a>
            </td>
        </tr>
    </tbody>
</table>

