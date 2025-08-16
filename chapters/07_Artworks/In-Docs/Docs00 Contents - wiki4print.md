---
cssclasses:
  - docs
---
<div id="banner">
<a href="https://wiki4print.servpub.net/index.php?title=Docs:00_Contents#Index_of_Sections">
<img src="media/W4P_logo.png"/>
</a>
</div>

# [Docs:00 Contents - wiki4print](https://wiki4print.servpub.net/index.php?title=Docs:00_Contents#Index_of_Sections)

These docs make up the process and steps that made up the back-end of our technical configuration. These docs act not only as a resource as to how to take up and hack these VPN infrastructures for yourself, but also to present alongside this the practices, networks and inspirations that have led us to this infrastructure's existence.

## Index of Sections

-   [01 Setup a Local Collaborative Environment](https://wiki4print.servpub.net/index.php?title=Docs:01_Setup_a_Local_Collaborative_Environment "Docs:01 Setup a Local Collaborative Environment")
-   [02 Local Server Setup with Nginx](https://wiki4print.servpub.net/index.php?title=Docs:02_Local_Server_Setup_with_Nginx "Docs:02 Local Server Setup with Nginx")
-   [03 VPN with Tinc](https://wiki4print.servpub.net/index.php?title=Docs:03_VPN_with_Tinc "Docs:03 VPN with Tinc")
-   [04 Reverse Proxy with NginX](https://wiki4print.servpub.net/index.php?title=Docs:04_Reverse_Proxy_with_NginX "Docs:04 Reverse Proxy with NginX")

## Prerequisites

If you would like to follow along, the following are necessary:

-   **Small board computer (SBC)**
	-   We used a raspberry pi, although You don’t necessarily need to use a pi to create a collaborative environment, you could use another type of computer. To understand more about why we chose to use a pi, you can find our notes here [Chapter 2a: Server Issues: Platform Infrastructure](https://wiki4print.servpub.net/index.php?title=Chapter_2a:_Server_Issues:_Platform_Infrastructure "Chapter 2a: Server Issues: Platform Infrastructure")
-   **Peripherals**
    -   HDMI, screen, keyboard, mouse etc.
-   **A laptop or other personal computer**
    -   It would be good to have SSH installed on your laptop. Most OS have it by default now, if not then manually install following the steps under [01.3 SSH](https://wiki4print.servpub.net/index.php?title=Docs:01.3_SSH "Docs:01.3 SSH")
-   **Knowledge of terminal/bash**
    -   For an intro to basic terminal/bash commands see [00.2 Terminal Unix Commands Cheat Sheet](https://wiki4print.servpub.net/index.php?title=00.2_Terminal_Unix_Commands_Cheat_Sheet "00.2 Terminal Unix Commands Cheat Sheet")

## Foundational information

If you're new to sever-ing and sysadmin, you may find the following guides useful:

-   [00.1 Network terminology](https://wiki4print.servpub.net/index.php?title=Docs:00.1_Network_terminology "Docs:00.1 Network terminology")
    -   Gives an overview of terms we will be using throughout this guide in relation to networking
-   [00.2 Terminal Unix Commands Cheat Sheet](https://wiki4print.servpub.net/index.php?title=Docs:00.2_Terminal_Unix_Commands_Cheat_Sheet "Docs:00.2 Terminal Unix Commands Cheat Sheet")
    -   Is an introduction to working on the command line.

## Access

We have tried to make these docs accessible and legible (as possible) to both technical and non-technical reading. We have done this through not only try to follow the [Web Content Access Guidelines](https://www.wcag.com/resource/wcag-quick-tips-for-content-writers/) but also working with the concept of *semi-plain* language that Kelsie Acton notes in here chapter *Plain Language for Disability Culture* in [Crip Authorship](https://nyupress.org/9781479819362/crip-authorship/). Acton states this as:

> Note on writing: This chapter is written in what I call a semi- plain language style. This means I do the following:
> 
> -   Use an active voice
> -   Mostly use the 6000 most common words in the English language
> -   Use short sentences
> -   Use 14 point font
> -   Use “I” and “you”

We may also use "us" and "we" to state In-grid and our collaborators making this infrastructure.

If you want a light, but still deep exploration of the setup, check out the [Index of each section](https://wiki4print.servpub.net/index.php?title=Docs:00_Contents#Index_of_Sections) listed above.

If you have any access requests, please email: in-grid@in-grid.io