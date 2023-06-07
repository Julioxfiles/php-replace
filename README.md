# php replace 
It works from the Windows/Linux terminal.

## php replace -f fileToBeReplace.php,anotherFile.txt -w fileWithDataToReplace.json 

## php replace -d directoryWhereFilesWillBeReplaced -w fileWithDataToReplace.json -r true

php replace is a php program that works from the Windows or Linux command line and is capable of replacing the content of a file or series of files followed by commas or one directory and its sub-directories with the data specified in an array taken from a json file.

For this example, I'll use the words.json file. You can call whatever you want.
Here is the content.

````
  [ 
    {"replace":"this text","with":"This other text"},
    {"replace":"this text 2","with":"This other text 2"}
  ] 
````
  
  
## How to use it

  Examples:

  This command will replace the files fileOne.ext,fileTwo.txt in the current directory. The -l param will create a log file in the logs folder.

  ````
  $ php replace -f fileOne.ext,fileTwo.txt -w "words.json" -l file.log 
  ````

 This command will replace all the files in the directory "C:\xampp\htdocs\tests" with the content of the file words.json. The param -r true means it will read all sub-directories also. The -e vendor,.env.php will exclude the vendor directory and the .env file. The -l param will create a log file in the logs folder.
  
  ````
  $ php replace -d "C:\xampp\htdocs\tests" -w "words.json" -r true -e vendor,.env.php -l file.log 
  ````

### Params

-h - Display the list of params of the command.

-f - Represents a file or list of files follow by comas that will be replaced.

-d - Represents the directory that contains the files that will be replaced. The current    directory will be use if not is provided.

-r - Will read also the sub-directories into the given directory. Values: true, false.

-w - Represents a json file that contains an array of words to be found and replaced.

-e - Can exclude a file, a series of files, directory or list of directories follow by comas to be excluded.

-l - Can set the out put to a log file. Example: -l myfile.log


