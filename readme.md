next-twist
==========

Code and data supporting the blog post "Can language models predict the next twist in a story?"

Original texts (to the extent allowed by IP law) are in ```/chapterbooks```.

The script that iterates through texts, forming prompts and sending them to the API, is ```FourPassAnalysis.ipynb.``` Note that four passes were not performed on every text; some only got one pass, and  visualizations that discuss all twenty-five books only consider the first pass. Subsequent passes are only necessary if we want to catch all the chapter breaks.

The output from ```FourPassAnalysis``` is in ```/chapterout```.

Further analysis is performed on that output by ```AnalyzeFirstRunOfAll.ipynb``` (which produces the scatterplot of twenty-five novels against name_cloze data), and by ```ChapterAnalysis.ipynb``` (which produces the swarmplot for *Hound of the Baskervilles*).

The name_cloze data is drawn partly from [Chang et al 2023](https://arxiv.org/abs/2305.00118), and partly produced by ```NameCloze.ipynb```.

The visualization comparing model predictions to human predictions was based on a slightly different, older pipeline which allowed multiple sentences. For those scripts and data see ```/human-ground-truth```.

The folder ```/comparison-to-kld``` is a stub that I may flesh out as I do more tests. Right now it just illustrates the point that this method produces very different trends across narrative time than a method based on information-theoretical treatment of lexical data.



