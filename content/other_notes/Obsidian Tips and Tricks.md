---
title: Obsidian Tips and Tricks
---
## My hotkeys

| Intention           | Maneuver         |     |
| ------------------- | ---------------- | --- |
| Search for command  | `Command-p type` |     |
| Refactor            | ctrl + shift + r |     |
| toggle stacked tabs | ctrl + s         |     |
| workspaces          | Win + esc        |     |
| open today daily    | shift + alt + d  |     |
| open previous daily | shift + alt + <- |     |
### Internal Link to Folder or file outside of obsidian
When wanting to link to a file or folder outside of obsidian - 

Working Example:
- Taken notes in [file in this folder](<file:///C:\Users\giorgio\Box\GEDB Master Folder\Projects\P - ESG Holdings\ESG - Prospectus Checks>)

## Autocompleting commands
Use Autocomplete to do the following:

- Search for, find, and execute commands.

You might do this when you can't remember the exact hotkey or name, or maybe just because you just want to search and execute a command. 


### Search tips
You can filter out all of our daily notes from a search by adding the notation:
-tag:journaling

### Add box around text

> [!NOTE] box example
> sample text

### checkbox types (primary / blue topaz theme) 
- [/] In Progress
- [>] Rescheduled
- [<] Scheduled
- [!] Important
- [-] Cancelled
- [?] Question
- [*] Star
- [n] Note
- [l] Location
- [i] Information
- [S] Amount
- ["] Quote
- [I] Idea
- [p] Pro
- [c] Con
- [b] Bookmark
- [u] Up
- [d] Down
- [r] Rule/Law
- [L] Language/Translation
- [t] Time/Clock
- [T] Telephone

### add front-matter to all notes for publishing (in powershell)
in Linux type pwsh in terminal to access powershell

```
$files = Get-ChildItem -path /home/giorgio/Dropbox/ObsidianNotes -filter *.md -recurse -force
foreach ($file in $files)
{
   	$content = Get-Content $file.FullName
	$newString = "---
	`rtitle: " + $file.BaseName +"`r 
	---"
	Write-Output "================================ `r `n inserting" $newString " in" $file.FullName
	Set-Content $file.FullName -value $newString, $content
}

```

## quarts for publishing
### push updates
In future updates, you can simply run  the code below

```
npx quartz sync
```


### testing
Once you’ve [initialized](https://quartz.jzhao.xyz/#-get-started) Quartz, let’s see what it looks like locally:

```

npx quartz build --serve
```


This will start a local web server to run your Quartz on your computer. Open a web browser and visit `http://localhost:8080/` to view it.

## Internal Link to Folder or file outside of obsidian
When wanting to link to a file or folder outside of obsidian - 

Working Example:
- Taken notes in [file in this folder](<file:///C:\Users\giorgio\Box\GEDB Master Folder\Projects\P - ESG Holdings\ESG - Prospectus Checks>)