TECHNICAL DETAILS OF OUR CORPORA:

CORPUS 1 ‘FDR’:

Period: March 04, 1933 to April 12, 1945 (official beginning and end of FDR’s presidency). 
Search parameters: All documents on the American Presidency Project site within the above timeframe. Results further refined to only those spoken by FDR. Further refined by only those documents tagged as ‘spoken addresses or remarks,’ (to filter out noise from some policy papers, and bureaucratic writs and documents, focusing instead on the core of executive discourse). Also, for the sake of a coherent voice in the data.
Composition: 758 files. Including a range of spoken remarks from state of the union addresses, to remarks to various communities all around the US, to remarks to the press, remarks following discussions with foreign dignitaries, etc.
Here’s the link to these search results: https://www.presidency.ucsb.edu/advanced-search?field-keywords=&field-keywords2=&field-keywords3=&from%5Bdate%5D=03-04-1933&to%5Bdate%5D=04-12-1945&person2=200288&category2%5B%5D=8&items_per_page=100

Total word count: 1,092,549

Average word count per speech: 1,441.36


CORPUS 2 ‘REG’:

Period: January 20, 1981 to January 20, 1989 (official beginning and end of Reagan’s presidency). 
Search parameters: All documents on the American Presidency Project site within the above timeframe. Results further refined to only those spoken by Reagan. Further refined by only those documents tagged as ‘spoken addresses or remarks,’ (to filter out noise from some policy papers, and bureaucratic writs and documents, focusing instead on the core of executive discourse). Also, for the sake of a coherent voice in the data.
Composition: 2,990 files. Including a range of spoken remarks from state of the union addresses, to remarks to various communities all around the US, to remarks to the press, remarks following discussions with foreign dignitaries, etc.
Here’s the link to these search results: https://www.presidency.ucsb.edu/advanced-search?field-keywords=&field-keywords2=&field-keywords3=&from%5Bdate%5D=01-20-1981&to%5Bdate%5D=01-20-1989&person2=200296&category2%5B0%5D=8&items_per_page=100

Total word count: 4,894,246

Average word count per speech: 1,636.87

SCRAPING METHOD:

We used the web-scraper Chrome Plugin, and in batches of 100 (all that my browser could cope with!) programmed it to scrape the text of every document returned in the searches on the American Presidency Project website detailed above. The output consisted of XLSM files containing batches of 100 speeches with each new line on a new row. 
 
 PROCESSING METHODS:
 
We ran various python scripts to do the following: read through the XLSM files and identify individual speeches, inserting a marker between them. Another script transfers every speech into its own unique JSON file with the date of the speech (in a sortable format) and its title as the title of the JSON file. A third script cleaned up the JSON files a little, removing some extraneous dashes and quotation marks.
We also created datasets of extracted Q and A exchanges from each corpus. Q and A pairs like these can be really useful for machine learning experiments. 

NOTE: Some of the titles of these speeches created file names that were longer than the Windows cap of 260 character-length file names, so we created a feature that simply truncates file names that are longer than this limit. So be aware that some of the longer speech titles may appear to be strangely truncated. The key bits, including the date, and the start of the title are retained, and in any case the full title is reproduced within the contents of the JSON file. 

