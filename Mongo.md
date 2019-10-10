In mongoDB you can use regular expression object (i.e. /pattern/)

# $regex

```{ <field>: { $regex: 'pattern', $options: '<options>' } }```

```{ <field>: { $regex: /pattern/<options> } }```

# $options

| options | description                                       | example                                                     | result                          |
| ------- | ------------------------------------------------- | ------------------------------------------------------------| --------------------------------|
| i       | Case insensitivity ```to match upper and lower``` | db.products.find({ sku: { $regex: /^ABC/i } })              | { "_id": 100, "sku": "abc123" } |
| m       | For patterns that include anchors (i.e. ^,$)      | db.products.find({ sku: { $regex: /^S/, $options: 'm' } } ) | { "_id": 100, "sku": "Sabc123" }|
| s       | Allows the dot character to match all character   | db.products.find( { description: { $regex: /m.*line/, $options: 'si' } } ) | { "_id": 102, "description": "Many spaces before line" } |
| x       | ignore white spaces and the comments              |||
