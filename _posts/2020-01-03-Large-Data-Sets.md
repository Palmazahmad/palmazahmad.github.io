--- 
title: Importing Large Data Sets
description: Tips and Tricks When Importing Extremly Large Data
dates: 03-01-2020 
category: Tech 
---

### Working With Large Data Sets ### 
Many people don't realise how difficult it can be when working with large data sets. Often people resort to using Excel to view and manipulate their data, this works sometimes **but not every time**. Excel has certain limitations which confine the data itself. These include: 

>Row limit of **1,048,576**  
>Column limit of **16,384**

This issue can be problematic especially if you work with large data sets. I personally had this problem as some imports held over 12 million records per Object / Class and Excel just wasn't the tool to use. 

#### If you want to view your Data there are some options available to you at this point: ####

**1\. Import into a Database**

Databases allow you to store data in fields and tables with no limit in size. You can set constraints on the  fields too, to match your data. The Database is really your choice but lately I've been using [Postgres](https://www.postgresql.org). The syntax is slightly different to mysql but its really simple to use. Once you have everything set up and ready to go all you have to do is import your data. Depending on the number of fields - I set the fields myself as you have control on the data types and other extras such as 'Not Null', 'Primary Key' etc. And that's it. Now you can use SQL to query the data. 

If you're using Postgres Pg4 admin tool, to view all your data use this: 
```SQL
SELECT * 
FROM public."TABLENAME"
```

>One annoying problem is unlike other major data management studios it doesn't include the functionality of reading the first column lines as fields automatically. 

**2\. Power Pivot (In Excel)**

If you want to stick to excel but have too much data you can use Power Pivot. This tool allows you to analyse large datasets, it can handle 100+ million rows. It's considered as using a pivot table for a large dataset. 

It's great when it comes to importing data from multiple source. This means you can import .SQL, .txt, Access database document and others. This gives you the freedom of being able to Import any type of data file, even if your data is in a standard text file. (Please use CSV...)

**3\. Microsoft Access

This tool is another database but simpler format. You can straight type or enter what settings you want and import data easily using .CSV. This is great if you have never used SQL or not too great at it. 

<br> 

### Overall ### 
There are other ways to import large data which I haven't mentioned above but these are the most common. Especially if you want to view and manipulate it. I personally prefer the database method as I can call and edit what I want and using SQL is much easier for me rather than click and drag. 
