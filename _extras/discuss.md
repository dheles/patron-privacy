---
title: Discussion
---
## About ZIP codes

While ZIP Codes can serve as a preferable alternative to specific (US) street addresses, they aren't without issues. First, outliers in your data who happen to be among the few (or only) individuals who reside in a given ZIP Code will not be afforded adequate privacy protection. Second, ZIP Codes to not correspond to geographic areas in the way many of us assume them to. Depending on your reasons for collecting and analyzing patron address data, this may or may not be a problem. The use of ZCTAs (ZIP Code Tabulation Areas) can help address both of these issues. ZCTAs are a system developed by the US Census Bureau to aggregate postal ZIP Codes into geographic areas. Using them makes it possible to map aggregated data (using a Geographic Information System (GIS). Because there are fewer ZCTAs than ZIP Codes, outliers in you data MAY be included in larger population groups, and thus less subject to re-identification. Obviously, you would want to re-check your results to confirm that this is true for your specific data. All of this insight comes to us from this excellent article in the Code4Lib Journal by Frank Donnelly, of the City University of New York: [Processing Government Data: ZIP Codes, Python, and OpenRefine](https://journal.code4lib.org/articles/9652). The article not only explains ZCTAs and their use, it also shares python code that can be used or modified for this purpose. We are grateful for this excellent resource and highly recommend it for further reading.

{% include links.md %}
