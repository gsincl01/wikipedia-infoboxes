# wikipedia-infoboxes

## Background
This repository contains the query and processing code to support the publication "Wikipedia curation and the US-EPA CompTox Chemicals Dashboard."

## Abstract
The online encyclopedia Wikipedia aggregates a large amount of data on chemistry, encompassing well over 20,000 individual Wikipedia pages, to serve the general public as well as the chemistry community. Many other chemical databases and services utilize this data, and previous projects have focused on methods to index, search, and extract it for review and use. We present first a new and comprehensive effort which combines bulk automated data extraction over tens of thousands of pages, semi-automated data extraction over hundreds of pages, and fine-grained manual extraction of individual lists and compounds of interest. We then correlate these data with the existing contents of the U.S. Environmental Protection Agency’s Distributed Structure-Searchable Toxicity database to 1) characterize the completeness and accuracy of the overall chemical space on Wikipedia, 2) evaluate the available data on sets of interest, such as synthetic cannabinoids, in both DSSTox and Wikipedia, and 3) facilitate bidirectional linkage of detailed chemistry and usage information from Wikipedia with expert-curated structure and identifier data from DSSTox for a new list of nearly 20,000 chemicals.

## Usage
The WikipediaInfoboxesMain.java class will download and parse the contents of all Wikipedia pages embedding the Chembox or Drugbox template on first usage. On subsequent usages, it will download any new pages and archive the previous download; it can also be configured to redownload all pages instead of just finding pages added since the last download. All downloaded and parsed data is stored in JSON files under a "data/" folder by default; folder locations and filenames can be reconfigured under WikipediaInfoboxesDict.java.
