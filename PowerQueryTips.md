# Data Journey Notes: Power Query Edition

Hellooo there! Brew yourself a fancy pour-over, kick back, because I’m about to drop some juicy tips on working with Power Query! 😜 
These aren't in any special order—just some things I've picked up over time that might help, whether you're just getting started or you're already knee-deep in data!

## My Detailed Tips

**Note:** Some of my advice overlaps with the [Power Query best practices](https://learn.microsoft.com/en-us/power-query/best-practices)—and if you see it here, that’s because I think it’s doubly important! 💡

### 1. Know Your Power Query Stuff: Types, Functions, and Specs!
Okay, real talk: you gotta know your data types! Why? Because some functions will straight-up break if you don’t use the correct type. 
Plus, it's always a good idea to make sure everyone knows what types they're dealing with. Trust but verify, amirite? 😉 You'd be shocked how many times someone claims a column is numeric, and then BAM—hello, random text values!

Power Query is like other ETL tools; it’s packed with prebuilt functions (a.k.a. "Functions by Category"). No need to reinvent the wheel if it’s already rolling smoothly. 
And hey, learn the syntax! You should at least skim through the specs so you know your operators, functions, and all that jazz.

- **Links:**
  - **[Data Types](https://learn.microsoft.com/en-us/power-query/data-types)**
  - **[Types](https://learn.microsoft.com/en-us/powerquery-m/m-spec-types)**
  - **[Functions by category](https://learn.microsoft.com/en-us/powerquery-m/power-query-m-function-reference)**
  - **[Specification](https://learn.microsoft.com/en-us/powerquery-m/power-query-m-language-specification)**

### 2. Dive Into Custom Functions
Alright, this is probably more advanced, but you’re gonna find yourself doing repetitive stuff. And what’s better than automating that? Learn to create custom functions, and you’ll save yourself a LOT of time!

- **[Custom Functions](https://learn.microsoft.com/en-us/power-query/custom-function)**

### 3. Organize Your Work!
Folders and meaningful names for queries, data connections, and resources will save your sanity. 
Trust me on this one.

### 4. Use Python When You Can!
If you know Python and you're allowed to use it (ugh, why doesn’t Power Query allow REGEX, c’mon Microsoft! 😒), then go for it! Jokes aside, there might actually be a good reason behind it… 
but honestly, learning a new syntax can be fun! It forces you to think differently about solving problems. BUT, if you're faster in Python and find yourself stuck in Power Query—switch over! 
Just make sure your workflow can handle it. Personally, I’ll hop back and forth depending on my workload because I use Power BI and like to keep things all in the Microsoft family. 
It’s all about that seamless integration… or so they say! 😉

- **[Use Python in Power Query Editor](https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-python-in-query-editor)**

### 5. Other Repos
Explore other repositories and take the time to learn from others' code. 
This can provide new perspectives, uncover techniques or best practices you might not have considered, and even highlight better alternatives to your own solutions.

- **[Lists in Power Query M](https://gorilla.bi/power-query/list-functions/)**
- **[M by lmkeF](https://github.com/ImkeF/M)**

### 6. Master GroupBy and Resphaping Tables
It took me forever to realize that Power Query had a GroupBy function just like Python’s Pandas library. 🤦‍♂️ 
Just select your group and all rows, and you can create tables for each group and perform whatever operations you need. Check out the "Functions by Category" table for more deets! 

Now, let’s talk about the other game-changer skill, the art of reshaping tables! 🙌 This comes in super handy when you’ve got turn a big, wide sheet cake into a beautiful stack of layered deliciousness. 
You know when you get a table that's so wide, it looks like it’s trying to win a “most columns ever” competition? 😂 But you need it in a long, tidy format for proper analysis or plotting. 
That’s where unpivoting steps in!

- **[Pivot](https://learn.microsoft.com/en-us/power-query/pivot-columns)**
- **[Unpivot](https://learn.microsoft.com/en-us/power-query/unpivot-column)**
- **[Transpose](https://learn.microsoft.com/en-us/power-query/transpose-table)**
- **[Grouping](https://learn.microsoft.com/en-us/power-query/group-by)**

### 7. DAX vs. M: Choose Wisely
So here's the deal: I use M for static or dimension tables (like slicing, filtering, or grouping data). DAX is for more dynamic, interactive stuff. 
For example, if I need to filter based on a field like an average, I’d create it in M and let users filter in the Power BI interface. 
But if they want to drill down into a hierarchy (like year, month, week), I’d use DAX so the averages update dynamically. Cool, right?

- **Food for thought:**
  - **[Dax or M Language](https://community.fabric.microsoft.com/t5/Desktop/Dax-or-M-Language/td-p/136827)**
  - **[Comparing DAX calculated columns with Power Query computed columns](https://www.sqlbi.com/articles/comparing-dax-calculated-columns-with-power-query-computed-columns/)**

### 8. Get Familiar with Data Imports

This is a BIG one. Learn how to read data from different sources—CSV, Excel, SharePoint, APIs, databases—you name it. 
And don’t just stick to the "clean" files. Practice with the messy, poorly structured ones. Trust me, you'll be grateful when you're handling weird CSV files that make Power Query throw a tantrum.

If you're new to data, go find some from sources other than Kaggle. You'll see what I mean. 😉

- **[Connectors in Power Query](https://learn.microsoft.com/en-us/power-query/connectors/)**

### 9. Learn Data Modeling
Get comfortable with the star schema—it's like the bread and butter of the industry!

- **[Build a star schema](https://learn.microsoft.com/en-us/power-query/dataflows/best-practices-for-dimensional-model-using-dataflows#build-a-star-schema)**

### 10. Lazy Change Type
Okay, this might be some lazy advice, but here goes: if the dataset is small (no greater than a GB), I usually let Power Query automatically detect the data type and then check for errors. 
For small datasets, this is easier than manually figuring out each type!

### 11. Enable Load… Wisely!
YOU DON’T NEED TO LOAD EVERYTHING INTO POWER BI! Yeahhh, save yourself some load time—disable the load for temp tables you’re using for your main table.

### 12. Learn the GUI and Scripting 
Every step in Power Query is saved, so check out the Advanced Editor for custom modifications. But for common transformations? 
The GUI has some pretty sweet shortcuts! Get familiar with it—you’ll thank yourself later.

- **[Interface](https://learn.microsoft.com/en-us/power-query/power-query-ui)**

And there you have it! A bunch of tips to help you navigate the wonderful world of Power Query. Hope this helps you level up!
