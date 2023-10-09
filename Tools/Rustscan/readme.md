 Why RustScan?

RustScan is a modern take on the port scanner. Sleek & fast. All while providing extensive extendability to you.

Not to mention RustScan uses Adaptive Learning to improve itself over time, making it the best port scanner for **you**.

## 🧋 Speed

![fast][speed-1]

Speed is guaranteed via RustScan. However, if you want to run a slow scan due to stealth, that is possible too.

Firstly, let's talk code.

We have tests that check to see if RustScan is significantly slower than the previous version. If it is, the continuous integration fails, and we can't commit code to master unless we make it faster.

[HyperFine][speed-2] is used to monitor RustScan's performance over time to answer the question, "Are we getting faster? Are we getting slower?".

Every pull request is reviewed by **one** person, but more often than not, **two** people review it. We test it manually and ensure the code doesn't negatively affect performance.

[Read more here][speed-3].

## ⚙️ Extensible

![scripts][extensible-1]

### _RustScan piping results into the custom Python script_

RustScan has a new scripting engine that allows anyone to write scripts in most languages. Python, Lua, and Shell are all supported.

Want to take your found ports and pipe them into Nmap for further analysis? That's possible. Want to run `smb-enum` if SMB is found open? Possible.

The possibilities are endless -- and you can write scripts in whatever language you feel comfortable with.

[Read more here][extensible-2].

## 🌊 Adaptive

![adaptive][adaptive-1]

### _RustScan automatically fine-tunes itself to match the host OS_

RustScan has a cool set of features called "Adaptive Learning". These features "learn" about the environment you are scanning and how _you_ use RustScan to **improve itself over time**.

We use this umbrella term for any feature that fits this criterion. The list constantly changes, so [check out our wiki for more information][adaptive-learning].

## 👩‍🦯 Accessible

![fast][accessible-1]

RustScan is one of the first penetration testing tools that aims to be entirely accessible.

[Most penetration testing tools are not accessible][accessible-2], which negatively affects the whole industry.

RustScan has continuous integration testing that aims to ensure it is accessible, and we are constantly working on ways to improve our accessibility and ensure _everyone_ can use RustScan.

INSTALLATION

Download the .deb file from the releases page:

https://github.com/RustScan/RustScan/releases

Run the command dpkg -i on the file.

Note: sometimes you can double click the file to achieve the same result.
