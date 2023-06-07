# php replace

php replace is a php program that works from the Windows or Linux command line and is capable of replacing the content of a file or series of files followed by commas or directories and subdirectories with the data specified in an array taken from a json file .

For this example, I'll use the words.json file. You can call whatever you want.
Here is the content.

````
  [ 
    {"replace":"this text","with":"This other text"},
    {"replace":"this text 2","with":"This other text 2"}
  ] 
````
  
  
## How to use it

  For example:
  php replace -d "C:\xampp\htdocs\tests" -w "words.json" -r true -e vendor,uno.php -l file.log 

-h Display the list of params of the command.,
-f Represents a file or list of files follow by comas that will be replaced.,
-d Represents the directory that contains the files that will be replaced. The current    directory will be use if not is provided.,
-r Will read also the sub-directories into the given directory. Values: true, false,
-w Represents a json file that contains an array of words to be found and replaced.,
-e Can exclude a directory or list of directories follow by comas to be excleded,
-l Can set the out put to a log file. Example: -l myfile.log,