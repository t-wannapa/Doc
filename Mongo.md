In mongoDB you can use regular expression object (i.e. /pattern/)

#Ex

```{ <field>: { $regex: 'pattern', $options: '<options>' } }```

```{ <field>: { $regex: /pattern/<options> } }```
