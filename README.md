# Allen_AI_Phecy

## Information Retrieval Based Method( lucene )

We build a local search engine using the wiki pages.  Then we merge the question and four answer together which become 4 querys. Then we use the 4 querys to search all the pages and get top@1 relevance. The answer respect to the highest relevance score will be choosen the result.
### Data Preparation

We collect 14176 keyword about science.(include ck12 and other science books)

### Usage 
	python allen_ai_predict.py 

---
detailed parameters

	python allen_ai_predict.py  -h
	usage: allen_ai_predict.py [-h] [--keywords KEYWORDS] [--get_data GET_DATA]
	                           [--index INDEX] [--qname QNAME]
	
	optional arguments:
	  -h, --help           show this help message and exit
	  --keywords KEYWORDS  keywords filename
	  --get_data GET_DATA  flag to get wiki data for IR
	  --index INDEX        flag to get wiki data for IR
	  --qname QNAME        file name for validation
	  
	  --get_data=1(download wiki pages)
	  --index=1(index wiki pages)

	
### folder info
	data/training_set.tsv traing data (not used)
	data/validation_set.tsv validation data
	data/keywords.txt 	 14176 keywords
	data/wiki_data/      total 13148 docs
	IndexFiles.index/    index build by pylucene

### Performance

We can get a score of 0.42000, please refer to https://www.kaggle.com/c/the-allen-ai-science-challenge/leaderboard for the current leaderboard.

### more detail
lucene version : lucene 4.10.1