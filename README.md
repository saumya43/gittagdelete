# gittagdelete
# steps of deleting tag from  specific date and older:
  
  # expire_tag.sh
   ```
   1: got list of tags with date
   2: run while loop to get all the tags older than specific date and of that specific date
   3: list all the tags to check if it is fetching correct tags we want to delete and then delete it. (list the tag on console to be sure that we delete the correct tag)
   4: trap() is used to fetch the ctrl_c interrupt an print the message.
   ```

# optional_argument.sh
    1: The script is  taking a few non-positional arguments/options: a date (string): tags of this date and older will be removed:
	                  example: --date 2021-02-17
    2: A repository path to operate upon:
                example: --repo https://github.com/kubernetes/kubernetes and is calling function  clone_git_repo() to clone that repo and cd into it.
    3: the script is invoked without any arguments/options or with -h option, the script print a usage   message and exit.

# pending work
 ```
 1: optional_argument.sh file is still not working properly.(need some debug help )
 2: whole project is  work in progress.
 3: dry-run command is work in progress.
 4: more efficient debug program is needed.
```

# some input for future work(implementing my ideas):
```
 1: expire_tag.sh file  will be build as a function and called into optional_argument.sh file.
 2: create an alias name $TAG_DELETE for the whole project , so whenever someone calls TAG_DELETE whole proces will run and will output the result:
     for_example : TAG_DELETE --date "2021-03-14" --repo "https://github.com/kubernetes/kubernetes" it will delete all the tags from date 2021-03-14 to older date from a https://github.com/kubernetes/kubernetes repo
```

