# nivo.cli.php.cmdwatch

while developing a command you will find yourself testing your classes over and over again. This means you launch your command and check if the result is what you did expect. If so you will add some more code and start over again. To get rid of this tedious task you can simple use cmdwatch to automatically execute the command you are working on once the file has saved.

To do so you simply have to do that:

> php bin/cmdwatch (pathToFileYouWantToObserve) (command that should then be executed)

cmdwatch will then wait for the file to be altered and executes the passed command afterwards

## Example

Lets say you are working on a task called `unicornify` placed under ~/bin/unicornify that is able to awesomely unicornify a passed string e.g. 'princess peach'. To keep cmdwatch observing that command and execute it the corresponding command could look like:

> php cmdwatch ~/bin/unicornify "php ~/bin/unicornify 'princess peach'"

Again, once your script gets saved the passed command gets executed. That way you can simply watch the results your change has produced.