`scriptlink` watches a folder for file changes. When a `.sh` or `.ps1` file changes, it executes the changed script using Bash or PowerShell, respectively.

I wrote this becuase I develop medical software which runs in an [air gap](https://en.wikipedia.org/wiki/Air_gap_(networking)). Well, it's not entirely air-gapped: the target hardware can access a file share. Using a web browser, I can log in to a frontend for the file share and deploy my code. I use the browser to copy my exe and DLL files, and when I'm ready to go live, I upload a script which `scriptlink` runs to bring down the current services, copy files from the file share to the local machine, and bring up the new services.

I wrote this while waiting for a flight in an airport terminal. I am just now learning Rust, so go easy.
