# SQL-Plot-tool

This is a small python based tool with `pydot` to visualize SQL query in a tree based structure.

Input should be nested lists query structure.

One example input: 

```python
tree2 = ['Query',
[
'cust_inv', ['cust', 'inv'],
'trk_s', ]
]
```

Output tree would be: 



More complex example input:

```python
tree3 = ['<query>', 
             ['HouseholdMetrics', 
                  ['HouseholdLoanSummary', ['LoanMetrics','HouseholdLoanDates','HouseholdOriginations'],
                   'HouseholdOriginations',
                   'HouseholdDepositSummary', ['HouseholdOriginations'],
                      'HouseholdWealthSummary', ['WealthMetrics','HouseholdOriginations'],
                   'HouseholdCustomerSummary',
                       ['CustomerMetrics', 
                        ['CustomerLoanSummary',  ['LoanMetrics'],
                         'CustomerDepositSummary',
                         'CustomerWealthSummary', ['WealthMetrics', ['WealthCustodianCustomerSummary']],
                         'CustomerHouseholdSummary',
                             ['HouseholdMaxCustomer', 
                              ['CustomerOriginations',
                               'CustomerLoanSummary',
                               'CustomerDepositSummary'],
                              'CustomerDepositSummary',
                              'CustomerLoanSummary', ['LoanMetrics',['LoanTrancheSummary'],],
                              'CustomerOriginations'],
                     'CustomerOriginations'],
                        'CustomerLoanSummary',
                        'CustomerHouseholdSummary']]
             ]
        ]
```

Output:

