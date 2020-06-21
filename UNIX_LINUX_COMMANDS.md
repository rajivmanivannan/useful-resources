# UNIX / LINUX Commands

## FILE SYSTEM

* ls — list items in current directory
* ls -l — list items in current directory and show in long
format to see perimissions, size, and modification date
* ls -a — list all items in current directory, including
hidden files
* ls -F — list all items in current directory and show
directories with a slash and executables with a star
* ls dir — list all items in directory dir
* cd dir — change directory to dir
* cd .. — go up one directory
* cd / — go to the root directory
* cd ~ — go to to your home directory
* cd - — go to the last directory you were just in
* pwd — show present working directory
* mkdir dir — make directory dir
* rm file — remove file
* rm -r dir — remove directory dir recursively
* cp file1 file2 — copy file1 to file2
* cp -r dir1 dir2 — copy directory dir1 to dir2
recursively
* mv file1 file2 — move (rename) file1 to file2
* ln -s file link — create symbolic link to file
* touch file — create or update file
* cat file — output the contents of file
* less file — view file with page navigation
* head file — output the first 10 lines of file
* tail file — output the last 10 lines of file
* tail -f file — output the contents of file as it
grows, starting with the last 10 lines
* vim file — edit file
* alias name 'command' — create an alias for a
command

- - -

## SYSTEM

* shutdown — shut down machine
* reboot — restart machine
* date — show the current date and time
* whoami — who you are logged in as
* finger user — display information about user
* man command — show the manual for command
* df — show disk usage
* du — show directory space usage
* free — show memory and swap usage
* whereis app — show possible locations of app
* which app — show which app will be run by default

- - -

## PROCESS MANAGEMENT

* ps — display your currently active processes
* top — display all running processes
* kill pid — kill process id pid
* kill -9 pid — force kill process id pid

- - -

## PERMISSIONS

* ls -l — list items in current directory and show
permissions
* chmod ugo file — change permissions of file to ugo u is the user's permissions, g is the group's
permissions, and o is everyone else's permissions.The values of u, g, and o can be any number between 0 and 7.
  * 7 — full permissions,
  * 6 — read and write only,
  * 5 — read and execute only,
  * 4 — read only,
  * 3 — write and execute only,
  * 2 — write only,
  * 1 — execute only,
  * 0 — no permissions.

* chmod 600 file — you can read and write - good for
files
* chmod 700 file — you can read, write, and execute good for scripts
* chmod 644 file — you can read and write, and
everyone else can only read good for web pages.
* chmod 755 file — you can read, write, and execute,and everyone
else can read and execute good forprograms that you want to share

- - -

## COMPRESSION

* tar cf file.tar files — create a tar named
file.tar containing files
* tar xf file.tar — extract the files from file.tar
* tar czf file.tar.gz files — create a tar with
Gzip compression
* tar xzf file.tar.gz — extract a tar using Gzip
* gzip file — compresses file and renames it to file.gz
* gzip -d file.gz — decompresses file.gz back to
file

- - -

## SEARCHING

* grep pattern files — search for pattern in files
* grep -r pattern dir — search recursively for
pattern in dir
* grep -rn pattern dir — search recursively for
pattern in dir and show the line number found
* grep -r pattern dir --include='*.ext —
search recursively for pattern in dir and only search in
files with .ext extension
* command | grep pattern — search for pattern in
the output of command
* find file — find all instances of file in real system
* locate file — find all instances of file using indexed
database built from the updatedb command. Much faster
than find
* sed -i 's/day/night/g' file — find all
occurrences of day in a file and replace them with night 
s means substitude and g means global - sed also
supports regular expressions

- - -

## SHORTCUTS

* ctrl+a — move cursor to beginning of line
* ctrl+f — move cursor to end of line
* alt+f — move cursor forward 1 word
* alt+b — move cursor backward 1 word

- - -
