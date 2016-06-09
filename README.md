# nivo.cli.php.cmdwatch

while developing a command for the command line you will find yourself testing your executables over and over again. This means you launch your command and check if the result meets your expectations. If so you will add some more code and start over again. To get rid of this tedious task you can simple use cmdwatch to automatically execute the command you are working on once the file has been saved.

To do so you simply have to do that:

> php bin/cmdwatch (pathToFileYouWantToObserve) (command that should then be executed)

cmdwatch will then wait for the file to be altered and executes the passed command afterwards

## Example

Lets say you are working on a task called `unicornify` placed under ~/bin/unicornify that is able to awesomely unicornify a passed string e.g. 'princess peach'. To keep cmdwatch observing that command and execute it the corresponding command could look like that:

> php cmdwatch ~/bin/unicornify "php ~/bin/unicornify 'princess peach'"

Again, once your script gets saved the passed command gets executed. That way you can simply watch the results your change has produced by just saving the file.

Sometimes your command takes advantage of external files. To tell cmdwatch to execute the passed command again (although the file itself might not been changed but the external files it is using) you can just hit any key.