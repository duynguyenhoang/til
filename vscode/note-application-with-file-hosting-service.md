# Use any File Hosting Service to create your own Note application

Note is one of the essential application for your daily work. I suppose you are struggling with selecting the most suitable application for you. Using with your laptop, sync it to your Android phone or your iPad.

- Why don't you use utilize File sync provided from File Hosting Service?
- Why don't you use your favourite IDE to modify your note?

## How?

- Use your favourite File Hosting Service provider which support auto sync (I use Dropbox)
- Add new alias `alias note="code $HOME/Dropbox/notes/"` to your `~/.bashrc`, `$HOME/Dropbox/notes/` is the note location and it is inside Dropbox folder and Dropbox to sync this location automatically, `code` is your VScode 😉
- Open new terminal and type `note`
- Hopefully you can see VSCode appear, create your new note file
- See new file appears on your Dropbox too.

## Need more?

- You can definitely create some template files with some defined sections for your different purposes. 
- Then create alias/function to create note automatically from those templates

Here is my example, call `nnote` to create daily note automatically. Straitforward isn't it? 💃

```bash
nnote () {
    # File name should be 20200115.md
	DAILY_FILE="$HOME/Dropbox/notes/DailyNotes/$(date '+%Y%m%d').md"
	if [ -f "$DAILY_FILE" ]
	then
		echo "Note $DAILY_FILE exists"
	else
		cp $HOME/notes/templates/daily_note.md ${DAILY_FILE}
	fi
}
```
