London Lives Coroners' Inquests
=====================

[London Lives 1690-1800: Crime, Poverty and Social Policy in the
Metropolis](http://www.londonlives.org) is an online resource
providing 'a wide range of primary sources about eighteenth-century
London, with a particular focus on plebeian Londoners'. The site includes three series of [coroners' inquests](https://www.londonlives.org/static/IC.jsp): Middlesex; City and Southwark; Westminster. So far (June 2018), I have compiled a catalogue of the Westminster inquests as a finding aid and added plain text files of the formal inquisitions. I plan to do the same work for the other two series. 


This is version 2.0 of the data, updated in June 2018 to include text files of the Westminster inquisitions. The initial release of metadata only was in January 2018.


Westminster Coroners' Inquests, 1760-1799
--------------------

Inquests were usually held within a few days of a sudden, violent, accidental or unexplained death, at a local alehouse, parish workhouse or the location of the death itself. Deaths of prisoners in custody were subject to an automatic inquest. Most coroners came from a legal or medical background, and in Westminster they were appointed by the Dean and Chapter of Westminster Abbey.

The inquests produced a range of documents, usually bundled into a single set which uses the formal inquisition as its wrapper. The majority of Westminster inquests include depositions as well as the inquisition (the formal record of the inquest, its findings and verdict), warrants, jury lists and verdicts and other more miscellaneous papers. For example, sometimes there are letters or notes written to the coroner to inform him of a death, and suicide cases may include material written by the deceased.

I have been greatly aided in creating this dataset by the catalogue for the inquests 1760-1771 created by Tim Hitchcock, and some of the information from that dataset has been incorporated into this new data. I was also able to use the manually-compiled catalogue as a benchmark to test the semi-automated methods for identifying individual inquests in the London Lives XML data. 

As a result, although I haven't individually read most of the cases, I am confident that I have correctly identified virtually all inquests and the identity of their subjects. This was also aided by the original organisation of the Westminster inquests, and the fact that inquisitions were both highly regular in format (many are pre-printed forms, with gaps to fill in details of a case) and carefully written; as a result the transcriptions are more accurate than for many more informal London Lives documents. 

The information provided about verdicts and causes of deaths may be less reliable and should only be used as a guide. The data on causes of death was partly incorporated from Tim Hitchcock's catalogue of the inquests for 1760-1771.

The dataset
------

The dataset records 2894 inquests, giving dates, places, names of the deceased, verdicts and causes of death, and indicates inquests for children, prisoners in custody, and multiple deceased.. It does not include details of the various documents in each inquest, though it does note where depositions are present.

### metadata

**wa_coroners_inquests_v1-1.tsv** (January 2018)

| field | description |
|------|------------------|
| first_img | unique identifier, based on London Lives ID for the first image in the inquest |
| inquisition_img | London Lives image ID for the text of the inquisition |
| doc_date | dates (which should normally be the inquest dates) in most cases have been extracted from the London Lives XML, with any missing dates filled in manually |
| parish | parish names have been extracted from the inquisition text |
| the_deceased | the name(s) or other identifying information given for the deceased (eg "an unnamed woman")  |
| given | first name(s) of the deceased, if given. Abbreviated first names have been expanded, but nothing else has been done to standardise spelling variations.  |
| surname | surname of the deceased, if given  |
| gender | gender of the deceased, derived from first names where given; if the first name was not given, their gender was almost always stated at some point in the inquisition |
| verdict | a summary of the jury's verdict: accidental, natural causes, homicide, suicide, undetermined |
| cause_of_death | a summary of the cause or circumstances of death |
| deceased_additional_info | indicates if the deceased was a child or a prisoner, and the small number of inquests for multiple deceased  |
| has_depositions | 'y' if there are depositions for the inquest  |
| lonlives_url | London Lives URL for the first image in the inquest  |
| lonlives_document_ref | the London Lives document reference |
| source | archival source information |

# inquisition texts

2890 .txt files in [wa_inq_txt](wa_inq_txt)

The filename for each text is derived from London Lives image IDs, as used in the metadata, so that the files can easily be cross-referenced to the metadata and the website. 

Specifically, the filenames consist of **inquisition_img** and  the *numerical component* of **first_img**, separated by an underscore, eg:

    WACWIC652000005_652000004.txt

The plain text was extracted from the XML files using the Python BeautifulSoup library. Paragraph tags were replaced with line breaks and all other XML formatting was removed.

A small number of the inquests do not have corresponding inquisition texts because either the documents/images are missing, or the images have not been rekeyed.


### Further reading

* Fisher, Pam. *The Politics of Sudden Death: The Office and Role of the Coroner in England and Wales, 1726-1888*. Leicester University PhD, 2007. 
* Forbes, Thomas R., ‘Coroners’ Inquests in the County of Middlesex, England, 1819–42’, *Journal of the History of Medicine and Allied Sciences*, 32, no. 4 (1977).
* Forbes, Thomas R., ‘Inquests into London and Middlesex Homicides, 1675-1782’, *The Yale Journal of Biology and Medicine*, 50, no. 2 (1977).
* Forbes, Thomas R., ‘Deadly Parents: Child Homicide in Eighteenth– and Nineteenth–Century England’, *Journal of the History of Medicine and Allied Sciences*, 41, no. 2 (1986).
* Sharpe, James and J. R. Dickinson, ‘Coroners’ Inquests in an English County, 1600–1800: A Preliminary Survey’, *Northern History*, 48, no. 2 (2011).


Acknowledgments
--------

The data has been created using the transcriptions of the Inquests published at London Lives. I am deeply grateful to Tim Hitchcock and Bob Shoemaker, the London Lives project directors, for agreeing to share the data.

I also used a catalogue of the Westminster inquests for 1760-1771 previously created by Tim Hitchcock in the course of compiling this data, and with his consent have incorporated some of that data (particularly causes of death). I am also appreciative of his willingness to share his knowledge of the inquest documents.

The original documents are held at the Westminster Abbey Muniment Room.

The London Lives project (under the name Plebeian Lives) was funded by the Economic and Social Research Council between 2006-2010.

Re-use
---------

The dataset and all accompanying documentation are licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

This means that you are free to copy and redistribute the material in any medium or format; and to remix, transform, and build upon the material for any purpose, even commercially, providing you follow the terms of the licence:

-    You must give appropriate credit, provide a link to the license, and indicate if changes were made.
-    If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.


Citation
--------

Suggested citation:

Sharon Howard, A Catalogue of Westminster Coroners' Inquests 1760-1799, version 2.0 (2018), based on data from *www.londonlives.org*.
