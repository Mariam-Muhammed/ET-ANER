CANERCorpus is a Classical Arabic NER corpus, which is manually annotated (Salah and Zakaria 2018). 
This corpus contains over 7,000 Hadiths (sayings of Prophet Muhammad) extracted from the Sahih Al-Bukhari book. 
The annotations include 20 named entity classes. These classes include person (Pers), location (Loc), organization (Org), measurement (Meas), money (Mon), book (Book), date (Date), time (Time), clan (Clan), natural object (NatOb), crime (Crime), day (Day), number (Num), God (Allah), prophet (Prophet), religion (Rlig), sect (Sect), paradise (Para), hell (Hell), month (Month) and other (O).  
The corpus contains a total of approximately 72,108 named entities. 
In this study, we only used eight named entities labeled as: Pers, Allah, Prophet, Loc, Clan, Date, NatOb and other (O), because the rest of entities are insufficient to train the model.
We also excluded the named entities labeled as “NUM” because 93.33% of (Num) entities were page numbers, which may slightly cause fake improvement in the model performance. 

The CANERCorpus dataset lacks marked sentence boundaries with a dot. 
To address this, we determined the average sentence length in the Sahih Al-Bukhari book, which is 38 words. 
We employed this threshold to establish sentence boundaries, adding a dot after every 38 words. 
Prior to marking the sentence's end, we ensure that the last word is labeled with the named entity "other (O)" to prevent the disruption of related entities. Finally, we divided the dataset randomly into three subsets: approximately 80% served as the training dataset, around 10% as the validation dataset, and another 10% as the testing dataset. 
