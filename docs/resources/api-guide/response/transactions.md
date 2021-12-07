## Transactions

| Element / property | Description |
| --- | --- |
| RqUID | Unique Request Identifier. The Client Site sends this element with the request. |
| FILoginAcctList | List of FI Login Accounts from which the selected transactions are to be returned. |
| SearchCriterion | The search criterion for which transactions are required. |
| TrnType | Transaction type. Possible values: Debit, Credit |
| SelRangeDt | The date range for which transactions are to be returned. |
| SelRangeAmt | The amount range for which transactions are to be returned. |
| StartAmt | Start amount of amount range. Note: Presently, the Currency code is ignored while performing the search, and results in all currencies are returned, regardless of the currency code specified in the search. |
| EndAmt | End amount of amount range. Note: Presently, the Currency code is ignored while performing the search, and results in all currencies are returned, regardless of the currency code specified in the search. |
