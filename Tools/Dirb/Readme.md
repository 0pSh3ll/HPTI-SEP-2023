# Contributer 
Intern ID : HPTI-SEP23-048

| Name | Usage | Link |
| -------- | -------- | -------- |
| Dirb | Used to find the directories and files fn the website. | [Link](https://www.kali.org/tools/dirb/) |


## Introduction
`dirb` is a powerful tool for discovering directories and files on a website. It's commonly used to identify hidden or sensitive information.

## Installation
To install the `dirb` use the following commands.

***Note:*** Please note that these commands are considered for systems based on Debian Linux.

```bash
sudo apt install dirb
```

## Documentation
Here is the documentation of the `dirb` which provides basic idea of how to use this tool and also provides numbers of options that we can use with the tool to make our search more reliable.

```
-----------------
DIRB v2.22    
By The Dark Raver
-----------------

dirb <url_base> [<wordlist_file(s)>] [options]

========================= NOTES =========================
 <url_base> : Base URL to scan. (Use -resume for session resuming)
 <wordlist_file(s)> : List of wordfiles. (wordfile1,wordfile2,wordfile3...)

======================== HOTKEYS ========================
 'n' -> Go to next directory.
 'q' -> Stop scan. (Saving state for resume)
 'r' -> Remaining scan stats.

======================== OPTIONS ========================
 -a <agent_string> : Specify your custom USER_AGENT.
 -b : Use path as is.
 -c <cookie_string> : Set a cookie for the HTTP request.
 -E <certificate> : path to the client certificate.
 -f : Fine tunning of NOT_FOUND (404) detection.
 -H <header_string> : Add a custom header to the HTTP request.
 -i : Use case-insensitive search.
 -l : Print "Location" header when found.
 -N <nf_code>: Ignore responses with this HTTP code.
 -o <output_file> : Save output to disk.
 -p <proxy[:port]> : Use this proxy. (Default port is 1080)
 -P <proxy_username:proxy_password> : Proxy Authentication.
 -r : Don't search recursively.
 -R : Interactive recursion. (Asks for each directory)
 -S : Silent Mode. Don't show tested words. (For dumb terminals)
 -t : Don't force an ending '/' on URLs.
 -u <username:password> : HTTP Authentication.
 -v : Show also NOT_FOUND pages.
 -w : Don't stop on WARNING messages.
 -X <extensions> / -x <exts_file> : Append each word with this extensions.
 -z <millisecs> : Add a milliseconds delay to not cause excessive Flood.

======================== EXAMPLES =======================
 dirb http://url/directory/ (Simple Test)
 dirb http://url/ -X .html (Test files with '.html' extension)
 dirb http://url/ /usr/share/dirb/wordlists/vulns/apache.txt (Test with apache.txt wordlist)
 dirb https://secure_url/ (Simple Test with SSL)

```

## Basic Usage
To start using `dirb`, follow these simple steps:

1. Open your terminal.

2. Run `dirb` with the following command:
```bash
dirb <target-URL>
```
You cam replace `<target-URL>` with the website URL you want to scan.

![Dirb Basic]()

## Common Options
Here are some useful options you can use with `dirb`.

### `-w`: 
To use a custom wordlist. But in `dirb` it is not necessary to give wordlist, bydefault it use it's own wordlist called `common.txt` wich contains common name of directories or files.
You can use below command to use you custom wordlist:
```bash
dirb <target-URL> -w /path/to/wordlist.txt
```
Also dirb provides bunch of wordlists that you can use, this wordlists are available on `/usr/share/wordlists/dirb/` folder.

#### Example:
![Wordlist]()

### `-o`: 
Specify an output file to save the results. 

```bash
dirb <target-URL> -o /path/to/output.txt
```

#### Example:
![Output]()

### `-r`: 
This option is used to not search recursively, meaning it will only scan the specified target directory and not explore subdirectories.

```bash
dirb <target-URL> -r
```
This can be useful when you want to limit the scope of your scan to a specific directory.

***Note:*** Please note that these commands is different from `-R`.

#### Example:
![Recursive Scan]()

### `-x`: 
Exclude certain file extensions (e.g., `jpg,png`):
```bash
dirb <target-URL> -x .jpg,.png
```

- `-S`: Use SSL (HTTPS) for scanning:
```shell
dirb https://<target-URL>
```
