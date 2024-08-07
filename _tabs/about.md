---
# the default layout is 'page'
icon: fa-solid fa-address-card
order: 8
alt: "image alt text"
---

<!-- ![Furqonic](https://res.cloudinary.com/dlked0a5j/image/upload/v1716549244/photo_2024-05-24_18.13.35_g9fwb2.jpg) -->
![cheers](/assets/img/docimg/code1.jpeg){: w="1500" h="500" }
## Hey there,! Greetings from the other side of the world!👋
<br>
<hr>
 My Name is `Catur Mahdi Al Furqon` known As `Furqonflynn` (you can call me `alfynn`) 👋, <br>
I’m a full stack software engineer passionate about Web Development. <br> In this DOCS I just want to share what I know. <br>
My interests include: <span style="color: #FF0000 !important;">Web Scraping,Blockchain,Ethical Hacking,Hackintosh.</span> <br>
I am proficient in: <span style="color: #FF0000 !important;">HTML, CSS, JavaScript, Python, Java, PHP,Ruby,Perl,GO,SQL,Bash.</span>
<hr>

> For you `who` love Coding... you can try code below `written with GO` to see my Profile(Portofolio).
{: .prompt-tip }

## ❗️Coding is My Canvas... ➡️

```go
package main

import "fmt"

type Profile struct {
	Language  string
	Interest  string
	Instagram string
	Mastodon  string
}

func main() {
	me := &Profile{
		Language:  "HTML, CSS, JavaScript, Python, Java, PHP,Ruby,Perl,GO,SQL,Bash.",
		Interest:  "Web Scraping,Blockchain,Ethical Hacking,Hackintosh,and Tips&Trick.",
		Instagram: "@thesilentreal",
		Mastodon:  "@furqonflynn",
	}

	// Print profile information using formatted string
	fmt.Printf("Hi! My Name is %s.\n", "furqonflynn, (call me ‘alfynn) 👋! I just want to share what I know.\n"+
		"I’m a full stack software engineer passionate about Web Development")
	fmt.Println("I am proficient in:", me.Language)
	fmt.Println("My interests include:", me.Interest)
	fmt.Println("Follow me on Instagram:", me.Instagram)
	fmt.Println("Connect with me on Mastodon:", me.Mastodon)
}
```
> `Without` color output!
> {: .prompt-warning }

```go
package main

import (
	"fmt"

	"github.com/fatih/color"
)

type Profile struct {
	Language  string
	Interest  string
	Instagram string
	Mastodon  string
}

func main() {
	me := &Profile{
		Language:  "HTML, CSS, JavaScript, Python, Java, PHP,Ruby,Perl,GO,SQL,Bash.",
		Interest:  "Web Scraping,Blockchain,Ethical Hacking,Hackintosh,and Tips&Trick.",
		Instagram: "@thesilentreal",
		Mastodon:  "@furqonflynn",
	}

	// Print profile information using color package

	// Welcome message
	welcome := color.New(color.FgHiCyan)
	fmt.Println(welcome.Sprint("Hi! My Name is "), color.New(color.Bold).Sprint("furqonflynn, (call me ‘alfynn) !"))
	fmt.Println(welcome.Sprint("I just want to share what I know.\n"))
	fmt.Println(color.New(color.FgGreen).Sprint("I’m a full stack software engineer passionate about Web Development"))
	// Skills and Interests
	fmt.Println(color.New(color.FgHiMagenta).Sprint("\nI am proficient in:"))
	fmt.Println(me.Language)
	fmt.Println(color.New(color.FgHiMagenta).Sprint("\nMy interests include:"))
	fmt.Println(me.Interest)
	// Social Media
	fmt.Println(color.New(color.FgYellow).Sprint("\nFollow me on Instagram:"), me.Instagram)
	fmt.Println(color.New(color.FgYellow).Sprint("Connect with me on Mastodon:"), me.Mastodon)
}

```
> `With` color output! using package [/fatih/color](https://github.com/fatih/color)

> You need to install the fatih/color package:
{: .prompt-tip }

Use the following command:
```bash
go get -u github.com/fatih/color
```
> Just run the code, to see my Profile. `XD`
{: .prompt-tip }
> With the `command` below!
```bash
go run profile.go
```
{: file='_MyProfile/profile.go'}
<br>
## 📬 Get in touch

[![Telegram](https://img.shields.io/badge/Telegram-DMme-orange)](https://t.me/edwinbagas7)
[![EMAIL](https://img.shields.io/badge/Email-caturmahdialfurqon-blue)](mailto:caturmahdi.alfurqon@icloud.com)
<br>
## 🤜🏻🤛🏻 For Support

You can support me.

[![Furqonic](https://img.shields.io/badge/SUPPORTME-Coffee-succsess.svg?style=flat)](https://pastebin.com/raw/Z57X2iwX)
<br>
[![Paypal Furqonic](https://img.shields.io/badge/USD$-Paypal-informasional.svg?style=flat)](https://paypal.me/caturmahdialfurqon)
<br>
[![BSC Furqonic](https://img.shields.io/badge/ETH-0x07Fe74030B01B1F9A9c2699929d7CAFDa66Ebf06-informational.svg?style=flat)](https://etherscan.io/address/0x07Fe74030B01B1F9A9c2699929d7CAFDa66Ebf06)
<br>
[![BTC Furqonic](https://img.shields.io/badge/BTC-bc1qf8d3fcl4zf08qy3ecz8jyw3cf8y8urd0s2g32s-informational.svg?style=flat)](https://pastebin.com/raw/Z57X2iwX)
<br>
[![DOGE Furqonic](https://img.shields.io/badge/SOL-73hvmQLGmfxXiJqvqiG2MwZReC9H3tFusZJGfffrBHpy-informational.svg?style=flat)](https://pastebin.com/raw/Z57X2iwX)
<br>
[![LTC Furqonic](https://img.shields.io/badge/MATIC-0x07Fe74030B01B1F9A9c2699929d7CAFDa66Ebf06-informational.svg?style=flat)](https://pastebin.com/raw/Z57X2iwX)
<br>
> Cheers to you!
{: .prompt-warning }
![cheers](/assets/img/docimg/Cheers2u.gif){: w="1500" h="500" }
