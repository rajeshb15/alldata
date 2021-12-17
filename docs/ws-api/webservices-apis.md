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
                This API is used to add/register the user with the AllData system.
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
                <b>Note:</b> Users with &quot;Admin&quot; role cannot be added using this API; the AllData Professional Services team creates admin users during implementation.
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
                This API is used to unregister a previously registered user.
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
                This API is used to retrieve user profile information such as name, address, and contact details.
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

## updateUserProfile
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>updateUserProfile</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/UserMgmt/updateUserProfile</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is used to update user profile information such as name, address, and contact details.<br>
                <b>Note:</b> Fiserv does not validate address or email.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/User%20Management%20Service/updateUserProfile">updateUserProfile API docs</a>
            </td>
        </tr>
    </tbody>
</table>

## updateUserPassword
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>updateUserPassword</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/UserMgmt/updateUserPassword</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is used to change the password of the current user identified by the credentials in this request&#39;s SignonRq section.
                <li>Admin user&#39;s password cannot be modified using this request.</li>
                <br />
                <b>Note:</b> This API only updates the user password for a partner&#39;s customer AllData credentials. To update FI credentials, use the updateUserCredentials API.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/User%20Management%20Service/updateUserPassword">updateUserPassword API docs</a>
            </td>
        </tr>
    </tbody>
</table>

## signon
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>signon</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/UserMgmt/SignonRq</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is used to sign on to the AllData service. It authenticates the user and generates a session token. The session token can be used for subsequent calls and this token will expire after 18 minutes of ideal time.
                This session token is also required to launch the Add Account widget flow.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/User%20Management%20Service/signon">Signon API docs</a>
            </td>
        </tr>
    </tbody>
</table>


# External FI Seed Data Web services

This chapter lists each External FI Seed Data API in a table with a resource URL, descriptive information, and a link to Swagger documentation.

## getFinancialInstInfo
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>getFinancialInstInfo</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/SeedDataInq/getFinancialInstInfo</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API can be used in three different ways:
                <li>Retrieve FI IDs of all FIs Fiserv supports.</li>
                <li>Retrieve FI details given a set of FI IDs.</li>
                <li>Incremental refresh of FI seed data for a specific timeframe (typically every day).</li><br>
                This API also includes information about the extended services supported in an FI. When clients opt-in to such services, information on FI capability to support the service is included in this API response.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Seeded%20Data%20Inquiry%20Service/getFinancialInstInfo">getFinancialInstInfo API docs</a>
            </td>
        </tr>
    </tbody>
</table>


## searchFinancialInst
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>searchFinancialInstitution</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/SeedDataInq/searchFinancialInst</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                Provide at least three characters to search for FIs. Valid values for &#39;FIInfoRequired&#39; are:
                <ul>
                    <li>FIIDInfo - retrieves only IDs</li>
                    <li>FIIDInfoList - retrieves list of FIs with detail information</li>
                    <li>FINameInfoList – retrieves list of FIs with just ID and name</li>
                </ul>
                <li>By default, this API returns FI IDs.</li>
                <li>Use the &#39;FISearchSize&#39; parameter to limit the number of result records.</li>
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Seeded%20Data%20Inquiry%20Service/searchFinancialInst">searchFinancialInstitution API docs</a>
            </td>
        </tr>
    </tbody>
</table>


# External FI Messages Web service

This chapter presents the External FI Messages API in a table with a resource URL, descriptive information, and a link to its Swagger documentation.

## getFIMessageInfo
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>getFIMessageInfo</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/FIMessagesInq/getFIMessageInfo</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is used fetch the FI Messages (special instructions) connected to the institutions.It returns a collection of all FIs that have custom messages. Partners use this API on a periodic basis to collect FI specific messages and display them to their customers during the login flow.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/FI%20Messages%20Inquiry%20Service/getFIMessageInfo">getFIMessageInfo API docs</a>
            </td>
        </tr>
    </tbody>
</table>


# Account Management Web Services

This chapter lists each Account Management API in a table with a resource URL, descriptive information, and a link to Swagger documentation.

## initiateAddAccounts
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>initiateAddAccounts</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/AccountMgmt/initiateAddAccounts</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is also referred to as InitiateAddAccounts or HarvestAddRequest and is used to add new accounts or add more account to existing parent connection.
                <li>Requires FI ID, trust mode, and login parameters as an input.</li><br>
                This request is also used to send in MFA answers using the previously started HarvestID and additional login parameters requested.
                <li>If FI login parameters such as UserID or password are incorrect, error condition will occur with specific error code.</li>
                <li>Returns HarvestID (or run ID): Represents the running session at FI and is required while checking status.</li>
                <li>Returns FILoginAccountID: This identifier uniquely identifies the online login account of the user with an FI.</li>
                <li>If user tries to add the same login name again, &quot;Account already exists&quot; error (4300) occurs.</li><br>
                Refer to the [Add Account workflow (OAuth)](#_Add_Account_workflow_1) when invoking this API for OAuth-enabled FIs.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/initiateAddAccounts">initiateAddAccounts API Docs</a>
            </td>
        </tr>
    </tbody>
</table>


## getAddAccountStatus
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>initiateAddAccounts</td>
        </tr>
        <table>
            <tbody>
                <tr>
                    <td><b>Web Service Name</b></td>
                    <td>getAddAccountStatus</td>
                </tr>
                <tr>
                    <td><b>Resource URL</b></td>
                    <td>&lt;FiservWSUrl&gt;/AccountMgmt/getAddAccountStatus</td>
                </tr>
                <tr>
                    <td><b>Description</b></td>
                    <td>
                        This API is used to poll the status of InitiateAddAccounts.
                        <li>Requires HarvestID and RunID from &#39;initiateAddAccounts&#39; response</li>
                        <li>Response includes status of &quot;completed,&quot; &quot;harvest error,&quot; or &quot;in progress&quot;</li><br>
                        Check status periodically until service successfully harvests accounts, errors out, or times out.<br><br>
                        Handle errors such as login failure (301), multi-factor authentication (303), and wrong MFA answer (304) using the HarvestAddRq-AddMoreAccts element.
                        <br><br>
                        <b>Note:</b> Additional information is needed in case of MFA.
                        <br><br>
                        Refer to the [Add Account workflow (OAuth)](#_Add_Account_workflow_1) when invoking this API for OAuth-enabled FIs.
                    </td>
                </tr>
                <tr>
                    <td><b>Swagger</b></td>
                    <td>
                        <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getAddAccountStatus">getAddAccountStatus API Docs</a>
                    </td>
                </tr>
            </tbody>
        </table>
    </tbody>
</table>


## getNewAccounts
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>getNewAccounts</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/AccountMgmt/getNewAccounts</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is invoked after the initiateAddAccounts request has completed. It returns the list of financial accounts found on the FI website. At this point these accounts are not created in Fiserv database. The basic
                account information available after login to FI site is harvested, but information such as balance, transactions, and positions may not be available.<br/><br/>
                This API also includes account ownership information (full account
                number, account owner name, routing number, and contact information – address, email, and phone number) when clients opt-in for that extended service.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getNewAccounts">getNewAccounts API Docs</a>
            </td>
        </tr>
    </tbody>
</table>



## createAccounts
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>createAccounts</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/AccountMgmt/createAccounts</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                User can choose accounts to add within AllData for harvesting.
                <br><br>
                Fiserv classifies the harvested accounts based on certain account classification rules. The user can either override this classification or provide the classification if not already set.
                <br><br>
                After successfully adding accounts, call update account APIs to run on demand harvesting to retrieve account data.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/createAccounts">createAccounts API docs</a>
            </td>
        </tr>
    </tbody>
</table>

## deleteAccounts
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>deleteAccounts</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/AccountMgmt/deleteAccounts</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is used to delete either a parent CFI (FILoginAcctId) or a given financial account.
                <li>If a parent CFI ID is given, all associated financial accounts are also deleted.</li>
                <li>All account data including transactions and positions are deleted.</li>
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/deleteAccounts">deleteAccounts API Docs</a>
            </td>
        </tr>
    </tbody>
</table>

## updateAccountCredentials
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>updateAccountCredentials</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/AccountMgmt/updateAccountCredentials</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API can be used to update the user credentials information stored within AllData.After updating credentials in AllData, partner should validate the credentials by invoking on-demand account harvesting flow.
                <br><br>
                <b>Note:</b> This API is not applicable for OAuth-enabled FIs.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/updateAccountCredentials">updateAccountCredentials API docs</a>
            </td>
        </tr>
    </tbody>
</table>

## maintainAccount
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>maintainAccount</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/AccountMgmt/maintainAccount</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is used to modify nickname at Fiserv, account type, and properties such as retirement status.<br>
                Provide extended account type while modifying account type.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/maintainAccount">maintainAccount API Docs</a>
            </td>
        </tr>
    </tbody>
</table>


## addOfflineAccount
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>addOfflineAccount</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/ClientMgmt/addOfflineAccount</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is used to add offline accounts to client. Offline accounts are tangible assets not held in typical financial institutions. Examples of offline accounts are jewelry, automobiles, boats, RVs, rentals, paintings,
                and heirlooms.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Client%20Management%20Service/addOfflineAccount">addOfflineAccount API Docs</a>
            </td>
        </tr>
    </tbody>
</table>


## updateOfflineAccount
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>updateOfflineAccount</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/ClientMgmt/updateOfflineAccount</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API is used to modify client offline accounts.
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Client%20Management%20Service/updateOfflineAccount">updateOfflineAccount API Docs</a>
            </td>
        </tr>
    </tbody>
</table>

## addUpdateHostAccounts
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>addUpdateHostAccounts</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/AccountMgmt/addUpdateHostAccounts</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API used to add and update client banking/credit card accounts from host FIs.
                <br><br>
                <b>Add:</b> Account number, account name, and account type are mandatory elements to add client host accounts. Balance and transaction
                information are optional elements.
                <br><br>
                <b>Update:</b> The host accounts are identified using either combination of (FIId + AcctNumber) or AcctId in the API request.
                <li>If the combination of (FIId + AcctNumber) or AcctId matches between the AllData and the API request, the API updates the account attributes (balance, account name, transactions) in AllData.</li>
                <li>If the combination of (FIId + AcctNumber) or AcctId does not match, the API adds a new host account in the AllData system.</li>
                <li>The response API will notify the partner about the status of each host account processed as part of the request API.</li>
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/addUpdateHostAccounts">addUpdateHostAccounts API Docs</a>
            </td>
        </tr>
    </tbody>
</table>

## HostAccountsStatus
<table>
    <tbody>
        <tr>
            <td><b>Web Service Name</b></td>
            <td>HostAccountsStatus</td>
        </tr>
        <tr>
            <td><b>Resource URL</b></td>
            <td>&lt;FiservWSUrl&gt;/AccountMgmt/hostAccountsStatus</td>
        </tr>
        <tr>
            <td><b>Description</b></td>
            <td>
                This API returns the status of host accounts transaction categorization. Possible return values are:
                <li>InProgress</li>
                <li>Completed</li>
                <li>Failure</li>
            </td>
        </tr>
        <tr>
            <td><b>Swagger</b></td>
            <td>
                <a href="https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/hostAccountsStatus">hostAccountsStatus API Docs</a>
            </td>
        </tr>
    </tbody>
</table>

# Account Harvesting APIs

This chapter lists each Account Harvesting API in a table with a resource URL, descriptive information, and a link to Swagger documentation.

## updateAccounts

|

Web Service Name

 | updateAccounts |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/HarvestAccountData/updateAccounts |
| --- | --- |
|

Description

 | This API can be used to trigger on-demand account harvesting. Typically, all added accounts get harvested in nightly batch mode. If a user (or CSR) wants to see latest account data, partners can call this asynchronous API, poll the harvesting status and, after it completes, refresh the account data for the user.
- Updates all accounts of a user from list of FIs, all accounts under list of parent CFI IDs, or list of individual accounts
- Update accounts under a single parent CFI ID after the initial add.
- RunID and HarvestID returned in the response are required when checking call status.


This API also provides for requesting extended transactions history of the accounts on demand (any time) for the clients who opt in for that service. The request should include the ExtendedTrnsDays element with the number of days expected. |
|

Swagger

 | [updateAccounts API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/updateAccounts) |

## getHarvestStatus

|

Web Service Name

 | getHarvestStatus |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/HarvestAccountData/getHarvestStatus |
| --- | --- |
|

Description

 | The API returns the status of the update done in the updateAccounts API. Requires RunID and HarvestID from the updateAccounts response. This API has the IncludeDetail attribute that returns status based on the values passed. The typical values of this tag are &quot;FIStatus&quot; and &quot;AcctStatus.&quot;
- FIStatus: Returns the status of FIs specified in the updateAccounts API
- AcctStatus: Returns the status of accounts of FI. If the above values are not specified, API returns the status of all the accounts specified in the updateAccounts API.
 |
|

Swagger

 | [getHarvestStatus API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/getHarvestStatus) |

## getAccountUpdateSummary

|

Web Service Name

 | getAccountUpdateSummary |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/Account Data Inquiry Service/getAccountUpdateSummary |
| --- | --- |
|

Description

 | This API is primarily for clients using widget implementation. After users add accounts using the Add Account widget and the return URL is received from AllData, invoke this API to get the status of accounts update, before invoking the data pull APIs.

This API returns status of all accounts updated under that CEUserID within the last hour. |
|

Swagger

 | [getAccountUpdateSummary API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getAccountUpdateSummary) |

# Account Data Pull APIs

This chapter lists each Account Data Pull API in a table with a resource URL, descriptive information, and a link to Swagger documentation.

## getAccountsSummary

|

Web Service Name

 | getAccountsSummary |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getAccountsSummary |
| --- | --- |
|

Description

 | This API is used to fetch the account summary information for a specified FI account. |
|

Swagger

 | [getAccountsSummary API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getAccountsSummary) |

## getAccountDetails

|

Web Service Name

 | getAccountDetails |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getAccountDetails |
| --- | --- |
|

Description

 | This API can be used to fetch detail information about one or more FI login accounts of a user.
- It can be used to retrieve information about one or more login accounts.
- If no ID is specified, it returns information about all of user&#39;s FI login accounts.
 |
|

Swagger

 | [getAccountDetails API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getAccountDetails) |

## getInvestmentTrans

|

Web Service Name

 | getInvestmentTrans |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getInvestmentTrans |
| --- | --- |
|

Description

 | This API is used to fetch the transactions for an investment account. It returns the transactions for the specified date range. |
|

Swagger

 | [getInvestmentTrans API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getInvestmentTrans) |

## getCreditCardTrans

|

Web Service Name

 | getCreditCardTrans |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getCreditCardTrans |
| --- | --- |
|

Description

 | This API is used to fetch the transactions for a credit card account. It returns the transactions for the specified date range. |
|

Swagger

 | [getCreditCardTrans API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getCreditCardTrans) |

## getBankingTrans

|

Web Service Name

 | getBankingTrans |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getBankingTrans |
| --- | --- |
|

Description

 | This API is used to fetch the transactions for a banking account. It returns the transactions for the specified date range. |
|

Swagger

 | [getBankingTrans API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getBankingTrans) |

## getOtherAccountTrans

|

Web Service Name

 | getOtherAccountTrans |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getOtherAccountTrans |
| --- | --- |
|

Description

 | This API is used to fetch the transactions for other asset/liability/biller account. It returns the transactions for the specified date range. |
|

Swagger

 | [getOtherAccountTrans API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getOtherAccountTrans) |

## getTransactions

|

Web Service Name

 | getTransactions |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getTransactions |
| --- | --- |
|

Description

 | This API is used for searching for transactions in specified FI login accounts according to specified search criterion.

TrnType can be used to either retrieve debit transactions, credit transactions or both |
|

Swagger

 | [getTransactions API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getTransactions) |

## getDeletedTrans

|

Web Service Name

 | getDeletedTrans |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getDeletedTrans |
| --- | --- |
|

Description

 | This API is used to get the deleted transactions of all accounts in the home or by account group with a specified date range and row index of the batch.

The client/partner accumulating the transaction data in their system uses this API to remove the deleted transactions to avoid duplication of transactions in their system.

This process is referred to as &quot;transaction deduping&quot; and is performed to keep transaction data in sync between AllData and the FI. It updates the AllData system with any changes found in old transactions posted in the FI source. |
|

Swagger

 | [getDeletedTrans API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getDeletedTrans) |

## getInvestmentPos

|

Web Service Name

 | getInvestmentPos |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getInvestmentPos |
| --- | --- |
|

Description

 | This API is used to retrieve investment positions for an investment account. |
|

Swagger

 | [getInvestmentPos API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getInvestmentPos) |

## getEmployerStockOptions

|

Web Service Name

 | getEmployerStockOptions |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getEmployerStockOptions |
| --- | --- |
|

Description

 | This API is used to retrieve the stock options details of an ESOP account. |
|

Swagger

 | [getEmployerStockOptions API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getEmployerStockOptions) |

# Transaction Categorization APIs

Transaction categorization is an optional feature that can be turned on for partners that require AllData to categorize transactions. AllData can only perform this for banking and credit card account types.

This chapter lists each transaction categorization API in a table with a resource URL, descriptive information, and a link to Swagger documentation. See the AllData Transaction Categorization – API Specification document for more details.

## getTxnCategoriesInfo

|

Web Service Name

 | getTxnCategoriesInfo |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/SeedDataInq/getTxnCategoriesInfo |
| --- | --- |
|

Description

 | This API is used to get the transactions categories from the AllData system for a specific home.

Use Admin User role to get all the standard transaction categories and subcategories AllData provides. Clients must pull this complete standard set initially and later make this request to get any new category added or will be intimated to make this request if any new category added.

Use AllData User role to get custom subcategories created by the specific user. |
|

Swagger

 | [getTxnCategoriesInfo API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Seeded%20Data%20Inquiry%20Service/updateAccounts_1) |

## categorizeTransaction

|

Web Service Name

 | categorizeTransaction |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/TxnMgmt/categorizeTransaction |
| --- | --- |
|

Description

 | This API is used to assign/update the subcategory of transactions and apply this user choice to similar transactions in future.

This API can also be used to create a user-specific custom subcategory and assign it to transactions, and to apply the subcategory to similar future transactions. |
|

Swagger

 | [CategorizeTransaction API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Update%20Transaction%20Category%20Service%20PFM/categorizeTransaction) |

## deleteSubCategory

|

Web Service Name

 | deleteSubCategory |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/TxnMgmt/deleteSubCategory |
| --- | --- |
|

Description

 | This API is used to delete the custom subcategory created by specific user. |
|

Swagger

 | [DeleteSubCategory API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Update%20Transaction%20Category%20Service%20PFM/deleteSubcategory) |

# Budgets

This chapter lists each Budget-related API in a table with a resource URL, descriptive information, and a link to Swagger documentation. Budgets are used in PFM use cases.

## createBudget

|

Web Service Name

 | createBudget |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/BudgetMgmt/createBudget |
| --- | --- |
|

Description

 | This API is used to create budgets. |
|

Swagger

 | [createBudget API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Budget%20Management%20Service%20PFM/createBudget) |

## deleteBudget

|

Web Service Name

 | deleteBudget |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/BudgetMgmt/deleteBudget |
| --- | --- |
|

Description

 | This API is used to delete the budgets created by users. |
|

Swagger

 | [deleteBudget API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Budget%20Management%20Service%20PFM/deleteBudget) |

## editBudget

|

Web Service Name

 | editBudget |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/BudgetMgmt/editBudget |
| --- | --- |
|

Description

 | This API is used to edit the existing budgets. |
|

Swagger

 | [editBudget API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Budget%20Management%20Service%20PFM/editBudget) |

## findBudget

|

Web Service Name

 | findBudget |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/BudgetMgmt/findBudget |
| --- | --- |
|

Description

 | This API is used to find the status of user-created budgets and to track their progress. |
|

Swagger

 | [findBudget API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Budget%20Management%20Service%20PFM/findBudget) |

# Goals

This chapter lists each Goal-related API in a table with a resource URL, descriptive information, and a link to Swagger documentation. Goals are used in PFM use cases.

## createGoal

|

Web Service Name

 | createGoal |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/GoalMgmt/createGoal |
| --- | --- |
|

Description

 | This API is used to create a goal. |
|

Swagger

 | [createGoal API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Goal%20Management%20Service%20PFM/createGoal) |

## editGoal

|

Web Service Name

 | editGoal |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/GoalMgmt/editGoal |
| --- | --- |
|

Description

 | This API is used to edit the goal, changing its target amount, target date, or the contribution percentage of the account. |
|

Swagger

 | [editGoal API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Goal%20Management%20Service%20PFM/editGoal) |

## deleteGoal

|

Web Service Name

 | deleteGoal |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/GoalMgmt/deleteGoal |
| --- | --- |
|

Description

 | This API is used to delete a goal. |
|

Swagger

 | [deleteGoal API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Goal%20Management%20Service%20PFM/deleteGoal) |

## findGoal

|

Web Service Name

 | findGoal |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/GoalMgmt/findGoal |
| --- | --- |
|

Description

 | This API is used to find a goal and to check the status of the goal and the account(s) associated with it. |
|

Swagger

 | [findGoal API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Goal%20Management%20Service%20PFM/findGoal) |

# Bank Statement Download Services

This chapter lists each Bank Statement Download Services-related API in a table with a resource URL, descriptive information, and a link to Swagger documentation. AllData can download bank statements for a select list of FIs. By default, AllData can download up to three historical statements once customer consent is received. See the PDF Statement Download Service document for more details.

## bankStatementConsent

|

Web Service Name

 | bankStatementConsent |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountMgmt/bankStatementConsent |
| --- | --- |
|

Description

 | This API is used to provide user consent and FI consent to download bank account statements from the financial institution website.
- User consent and FI consent should be provided separately using this API.

- User consent is the primary consent, which is to be provided first.
- On providing user consent, AllData will set FI consent to true for all eligible FIs under the user profile.

- FI consent can be revoked in one or more FIs when the user does not wish to obtain statements from any specific FIs.
- FI consent can be provided again for consent-revoked FIs.
 |
|

Swagger

 | [bankStatementConsent API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/bankStatementConsent) |

## getBankStmtDetails

|

Web Service Name

 | getBankStmtDetails |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountDataInq/getBankStmtDetails |
| --- | --- |
|

Description

 | This API is used to get user and FI consent details and the details of the FIs and bank accounts under the user profile that are eligible for downloading the bank account statements.

It also includes the details of account statements available for download under each of those accounts.

**Note:** The availability of statements is dependent on connectivity with the source site. Refer to institution(s) or account(s) errors and resolve any associated issues to get the statements. |
|

Swagger

 | [getBankStmtDetails API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getBankStmtDetails) |

# Miscellaneous

This chapter lists each API in a table with a resource URL, descriptive information, and a link to Swagger documentation.

## GetWMAccessKey

|

Web Service Name

 | GetWMAccessKey |
| --- | --- |
|

Resource URL

 | \&lt;FiservWSUrl\&gt;/AccountMgmt/GetWMAccessKey |
| --- | --- |
|

Description

 | This API is used to generate WMAccessKey key for PCI compliance requirements for the FI. |
|

Swagger

 | [GetWMAccessKey API Docs](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/WMAccessManagement%20Service/GetWMAccessKey) |

© 2019-2021 Fiserv, Inc. or its affiliates. All rights reserved. This work is confidential, and its use is strictly limited. Use is permitted only in accordance with the terms of the agreement under which it was furnished. Any other use, duplication, or dissemination without the prior written consent of Fiserv, Inc. or its affiliates is strictly prohibited. The information contained herein is subject to change without notice. Except as specified by the agreement under which the materials are furnished, Fiserv, Inc. and its affiliates do not accept any liabilities with respect to the information contained herein and are not responsible for any direct, indirect, special, consequential or exemplary damages resulting from the use of this information. No warranties, either express or implied, are granted or extended by this document.

[http://www.fiserv.com](http://www.fiserv.com/)

Fiserv is a registered trademark of Fiserv, Inc.

Other brands and their products are trademarks or registered trademarks of their respective holders and should be noted as such.