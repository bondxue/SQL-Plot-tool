# SQL Plot Tool

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

<img src="https://github.com/bondxue/SQL-Plot-tool/blob/master/images/demo1.png" width="200">


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

<img src="https://github.com/bondxue/SQL-Plot-tool/blob/master/images/demo.png" width="800">
