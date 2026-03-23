# Programming Historian Lab Worksheet

Name: [Abhi Mummaneni]

## 1. What is the citation for the _Programming Historian_ lesson associated with this lab?

Stephen Krewson, "Extracting Illustrated Pages from Digital Libraries with Python," Programming Historian 8 (2019), <https://doi.org/10.46430/phen0084>.

## 2. What Python libraries does the lesson require you to download? (Use Markdown's list syntax to list them.)

- pip
- internetarchive
- requests
- gzip
- os
- xml.etree.ElementTree
- pathlib

## 3. What aspects, if any, of the lab are out of date? How would you fix them?

The lab used old api practices which were not necessary as we did not need to
create an api key for the internet archive. I would update the instructions
to show that the simpler workflow we used is possible. There are also a change
with the url for the internet archive as in the instructions they use iiif.archivelab.org
but we use iiif.archive.org. This can easily be fixed by just changing the url in the instructions,
but it would also be helpful to explain to the reader that the url may change and to check
the internet archive documentation for the current url. Furthermore, I would
include specific versions in the pip imports so that the instructions don't
need to be changed at the next breaking change of one of the packages.

## 4. What was the most important thing that you learned from this lab?

I learned how to efficiently query and retrieve data from the internet archive
using python. This will help in finding and analyzing large datasets.
Furthermore, I learned how to manipulate the returned data and work with the xml
format programmatically in python. I also learned how to work with different python
environments and debug their associated issues. Finally, I learned a method
which could be used for media specific analysis as the image data more closely represents
the original form of the text. This can be useful for analyzing literature in ways that
aren't possible just through text data alone.

## 5. Design and briefly outline a follow-up _Programming Historian_ lesson

What skills would you build on? How would you measure results?

I would include a continuation of this lesson that focuses more on analyzing the
retrieved data. This is difficult since the data is in xml format and represents images
but if there was ocr available we could do something similar to what we did with the
voyant lab and analyze the text data. The skills that we build on would be data handling
and manipulation. We can measure results by checking if data is downloaded and converted
into a correct format. Furthermore, for the analysis the lab could ask the students to
find certain trends in the data or certain word counts / analytics from the text data.
These values could be numerically checked, but it would be harder to measure more
abstract inferences from the data.
