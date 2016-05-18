Question Describe:

# Input: 

```python

	def some_api(self, rquest):
	    '''
	    describe

	    @Request(
	    (response-data note)
	    )

	    Or

	    @Request(
		(some/api/, get-some-data)
	    )

	    @Auth(admin)

	    @Response(
		(id, some-id),
		(name, some-name),
		(pay, ((id, pay-id),
		       (name, pay-name)
		       ))
	    )

	    @Errors(
		(404, can't find this person), 
		(409, confict id), 
	    )

	    @Author(minchiuan)
	    '''
```

# Output

	'''
	    descirbe

	    ## Auth:
	       admin

	    ## Author:
	       minchiuan

	    ## Request:
		auth: none | login | admin
		type: url | json
		example 1: Get user info
			{
				"key": "value",
				"key_2": "value_2"
			}

		exemple 2: Get user pay
			{
				"key": "value",
			}

	    ## Response:
		type: dict
		example:
			{
				"key": "value",
				"key_2": "value_2"
			}

	    ## Errors:
	        404: can't find this person.
		409: confilct id.

	'''
