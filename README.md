+ Shakespeare ML Intro 

This is a demo workbook that shows how the llm -> faiss pattern can be used to do analysis of some text. In this case Shakespeare's plays. 

To make the demo work you will need Python 3.8 and postgres 14. There is a create table string in the notebook that will get postgres up and going. 

The idea is to create a db of the embeddings so as to be able to play with FAISS and alter the indexing and so on quickly. The PG database is also used to deference the FAISS matches via the id field that FAISS returns when it looks up a nn. 

This is possibly not an ideal pattern because the embedding means that each row in the db is quite big - so for larger / real applications it's recommended to have another table that does this job. For this demo it's fine though. 

The analysis is done by finding all the "tokens" in the database of plays and then 
