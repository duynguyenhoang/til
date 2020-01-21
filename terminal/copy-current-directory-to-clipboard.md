# Copy your current directory to clipboard

Are you keyboard lover? Yes, I am. I use keyboard alot, but it is sometime difficult for me to copy the whole folder location. After some research, i have my own command to do that.

* Open your `~/.bashrc`
* Add new alias
  * Macos: `alias cpwd="pwd | xargs echo -n | pbcopy"`
  * Linux: `alias cpwd="pwd | xargs echo -n | xclip -sel clip"`
* Enjoy!

Note:

* `xargs echo -n` to remove new line
* For Linux please install `xclip`

