Question Describe:

# Input: 

```python

	def some_api(self, rquest):
	    '''
	    describe

	    @Request(
		{'/some/api/': 'get-information'}
	    )

	    Or

	    @Request(
		(*name*, string),
		(*phoen*, string),
		(password, string),
	    )

	    @Auth(admin)

	    @Response(
		(id, some-id),
		(name, some-name),
		(pay, ((id, pay-id),
		       (name, pay-name)
		       ))
	    )

	    @!(
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
	       auth: none | login | admin

	    ## Author:
	       minchiuan

	    ## Request:
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


# Sub Question:

  1. Change (key, value) to {"key": "value"}, change
     ((key, (sub-key-1, sub-value-1)) to
     {"key": {"sub-key-1": "sub-value-1"}}

     change [(key, value), (key2, value-2), (key3, value-3)]
     to [{"key": "value"}, {"key2": "value-2"}, {"key3": "value-3"}]

     change ((key1, value1), (key2, value2), (key3, value3))
     to {"key1": "value1", "key2": "value2", "key3": "value3"}