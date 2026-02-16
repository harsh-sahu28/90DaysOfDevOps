* Created an empty file
 -  touch notes.txt
 -  ls
 -  notes.txt

* Adding entries to notes.txt (> overwrite the file contents)
 - echo "Adding day 6 tasks to new file" > notes.txt
-  cat notes.txt
-  Adding day 6 tasks to new file

* Appending entries to notes.txt (>> appends entries)
  -  echo "Appending more tasks to the newfile" >> notes.txt
cat notes.txt
Adding day 6 tasks to new file
Appending more tasks to the newfile

* Used tail and head to view contents of notes.txt
   head -n 1 notes.txt
Adding day 6 tasks to new file
tail -1 notes.txt
Appending more tasks to the newfile
tail -2 notes.txt
Adding day 6 tasks to new file
Appending more tasks to the newfile


* Using tee to add and view the content added to the file at same time
  - echo "adding new text and viewing the file at the same time" | tee -a notes.txt
adding new text and viewing the file at the same time
- cat notes.txt
Adding day 6 tasks to new file
Appending more tasks to the newfile
adding new text and viewing the file at the same time



