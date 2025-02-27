# ICSH

## Tag 0.1.0 Interactive command-line interpreter
  - echo <text> : print text on the console
  - !!          : repeat the last command
  - exit <num>  : exit with the given exit code
  
## Tag 0.2.0 Script mode
  - ./icsh test.sh : return the input command content in the test.sh (in the current directory) to the console
  
## Tag 0.3.0 Running an external program in the foreground
  - run the command that already exist in SHELL

## Tag 0.4.0 Signal Handler
  - Ctrl+Z : to suspend the process in the current foreground (not your shell)
  - Ctrl+C : to kill the process in the current foreground (not your shell)
  - echo $? : to print the exit status code of the previous command. 
              You may assume that all build-in commands exits with exit code 0

## Tag 0.5.0 I/O redirection
  - reDir() : <Input/ >Output Redirection
  
## Tag 0.6.0 Background jobs and job control
  - command followed by "&" : will run as a background job
    - listed in the jobList[100] with 100 jobs limit
  - jobs : this command will list all the current jobs that are running/stopped
  - fg %<job_id> : Brings the job identified by <job_id> into the foreground 
    - does not continue, but start from the beginning
  - bg %<job_id> : Execute the suspended job identified by <job_id> in the background 
    - does not continue, but start from the beginning, run in fg instead

## Tag 0.7.0 Extra features
  - Allowing users to customize their prompt at the beginning of the program
    - Can type the prompt text
    - Choose a font color (pink/red/green/yellow/blue/white)
    - Choose styles (bold,underline)
    - Or choose the default version "icsh $ "
  - help() : this command return the instructions of this IC SHELL
  - !!!! : repeat the second last command

## Need to be done:
- echo $ --> needs to print previous exit number, but for now it prints 0 (idea: just save/call it from txt file inside the working directory)
- fg %<job_id> (do not work properly) restarts the job instead ;P
- bg %<job_id> (do not work properly) restarts the job instead :P
- '!!' returns the prev command but when you call '!!' again nothing appears cus it saves prev '!!' in the history already (idea: set if command == '!!' then do not save it in the history)
