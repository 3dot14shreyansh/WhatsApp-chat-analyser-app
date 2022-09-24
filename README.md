# WhatsApp Chat analyser - Webbased App
This web based app aims to analyse WhatsApp chat between two indivdual or a group converstaion. 

- ### (1) Table of content



  - #### (1.1) Stop words
  
  
  
    - A text file which contains a stop word in english and hindi. This will help to filter out the stop word in chat analysis
   
   
   
  - #### (1.2) App
    - Used a web based service streamlit which is generally used for making simple project rather bulding things from scratch.
   
   
   
  - #### (1.3) Data cleaning / processing 
  
    Here two Python3 files have been used to handle the data set, one is
    
    - (1.3.1) preprocessor.py : Majorly resposible of drawing a dataframe using re(Regular expression) and Pandas library which seprates date of message arrived (it is further subcategorised with day column, month column, year column ), time of message arrived, text message message arrived, name / contact number of user.
    
    - (1.3.2) helper.py : With the help of library such as WordCloud, Pandas, Collections, URLextract and Emoji library some statical data was fetched such as total number message in a WhatsApp group / one on one converstaion, total number of words, total number of media shared, total number of links shared in the chats. It fetches the the user which is most active (in case of group). Other data which can also be achived are mothly chat time line, weekly chat timeline, daywise chat timeline and few other heat maps.
    
    
    
  -  #### (1.4) Requirnment : These are the libraries which is needed to run this app. 
     - streamlit 
     - matplotlib 
     - seaborn 
     - urlextract 
     - wordcloud 
     - pandas 
     - emoji <br />
    Consider running this code at the start after importing these files to your IDE inside your virtual environment : <br /> 
    pip install -r requirements.txt
    
    

  - #### (1.5) Setup
  
  
  
  - #### (1.6) Procfile
  
  
  
  - #### (1.7) .gitignore : to be ignored when running the app.
  
  
  
  
  
- ### (2) Errors :
    - (2.1) Emoji : This library might run on some OS and might not run on some OS, even if both OS are same.
    - (2.2) Date format : Depending upon the date stamp on your chat.txt : 
      - (2.2.1) Year format '22 then in code line 12 of processor.py paste this after removing the code of that line <br />
      df['message_date'] = pd.to_datetime(df['message_date'], format='%d/%m/%y, %H:%M - ')
      - (2.2.2) Year format 2022 then in code line 12 of processor.py paste this after removing the code of that line <br />
      df['message_date'] = pd.to_datetime(df['message_date'], format='%d/%m/%Y, %H:%M - ')
      
      
      
      
      
- ### (3) Output samples :
