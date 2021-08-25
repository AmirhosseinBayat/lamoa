# Lamoa
*Simple scala app help you get appropriate subtitle for given movie ;)*
## TODO Completion 
- [ ] **TECH**
    - HttpClient(STTP)
        - Http request to fetch html data
        - download file
    - CssSelector(JSOUP)
        - search and filter out html element 
---
- [ ] **Get path**
    - [ ] Autocomplete 
    - [X] Find And Filter out to get just video files (User can enter file name completely and in this case it gets to the next step)
        - List All available movies in the entered Directory
        - User selects video file  
---
- [x] **Extract Movie name**
    - pattern Registry
        - get the name of file and apply give pattern in *config file*
        - convert the name to standard name (THE(Separator such as /-_+...)MAURITANIAN -> The Mauritanian)        
        - Extract the name and other founded data to entity model such as year and quality (480p or 720p ...)
---
- [x] **Confirm from user**
    - Show extracted name to the user and user confirm if it is **Right**
        - unless user enter the name
    - confirm with IMDB
---
- [x] **Read Config**
    - Init: Languages to find (Default get ***EN*** Languages)
    - The Website URL to look up for find subtitle
---
- [x] **Download subtitles**
    - Search the extracted movie name in site
    - filter subtitles which is more match to file such as language,quality and the year
    -  download the first match
---
- [x] **Place subtitle files** 
    - Ensure the directory is writable
        - unless notify user directory is not writable (Cancel Process **OR** Specify the other Path to write the file)
    - rename the downloaded file to the name which user specified at first steps
    - save file
