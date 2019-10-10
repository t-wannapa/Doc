In mongoDB you can use regular expression object (i.e. /pattern/)

#$regex
```{ <field>: { $regex: 'pattern', $options: '<options>' } }```

```{ <field>: { $regex: /pattern/<options> } }```

#$options
| options | description                                       | example                                         | result                         |
| ------- | ------------------------------------------------- | ------------------------------------------------| -------------------------------|
| i       | Case insensitivity ```to match upper and lower``` | db.products.find({ sku: { $regex: /^ABC/i } })  | { "_id": 100, "sku": "abc123"} |

