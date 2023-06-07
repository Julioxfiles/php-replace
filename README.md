# php replace

This command reads an array from a json file. Example of it: 
  [ 
    {"replace":"this text","with":"This other text"},
    {"replace":"this text 2","with":"This other text 2"}
  ] 
  
  And search and replace it in a file or series of files followed by comma. 
  Or in an entire directory and subdirectories if you use -r true to do it.
  
## How to use it

  For example:
  php replace -d "C:\xampp\htdocs\tests" -w "words.json" -r true -e vendor,uno.php -l file.log 
