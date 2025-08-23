---
cssclasses:
  - docs
---
<div id="banner">
<a href="https://wiki4print.servpub.net/index.php?title=Docs:00_Contents#Index_of_Sections">
<img src="media/W4P_logo.png"/>
</a>
</div>


# [Docs:00 Contents - wiki4print](https://wiki4print.servpub.net/index.php?title=Docs:00_Contents)

![A diagram of the Servpub network infrastructure made by In-grid.](../media/Docs%20Infrastructure%20Diagram.jpeg)

A diagram of the Servpub network infrastructure made by In-grid.

## Introduction (\* ^ ω ^)

These docs offer up and share the processes and technical practices that made up the back-end of the Servpub network infrastructure. These docs aim to act not only as a resource to share how to take up and hack these VPN infrastructures for yourself, but also to present alongside this the practices, networks and histories that have emerged into the Servpub server infrastructures.

## Index of Sections

-   [01 Setup a Local Collaborative Environment](https://wiki4print.servpub.net/index.php?title=Docs:01_Setup_a_Local_Collaborative_Environment "Docs:01 Setup a Local Collaborative Environment")
    -   Learn how to set up a computer locally and how to make users, collectively connect and care for it.
-   [02 Local Server Setup with Nginx](https://wiki4print.servpub.net/index.php?title=Docs:02_Local_Server_Setup_with_Nginx "Docs:02 Local Server Setup with Nginx")
    -   Learn how to set up the computer as a server on your local network and host a basic HTML page!
-   [03 VPN with Tinc](https://wiki4print.servpub.net/index.php?title=Docs:03_VPN_with_Tinc "Docs:03 VPN with Tinc")
    -   Learn how to set up a Virtual Private Network (VPN) with Tinc so that you can have a portable server.
-   [04 Reverse Proxy with NginX](https://wiki4print.servpub.net/index.php?title=Docs:04_Reverse_Proxy_with_NginX "Docs:04 Reverse Proxy with NginX")
    -   Learn how to pass public internet traffic through the VPN to a site on the portable server.

## Prerequisites

If you would like to follow along in real life (IRL), you will need these bits of hardware!

-   **Small board computer (SBC)**
    -   We used a raspberry pi, although You don’t necessarily need to use a pi to create a collaborative environment, you could use another type of computer. To understand more about why we chose to use a pi, you can find our notes here [Chapter 2a: Server Issues: Platform Infrastructure](https://wiki4print.servpub.net/index.php?title=Chapter_2a:_Server_Issues:_Platform_Infrastructure "Chapter 2a: Server Issues: Platform Infrastructure")
-   **Peripherals**
    -   HDMI, screen, keyboard, mouse etc.
-   **A laptop or other personal computer**
    -   It would be good to have SSH installed on your laptop. Most OS have it by default now, if not then manually install following the steps under [01.3 SSH](https://wiki4print.servpub.net/index.php?title=Docs:01.3_SSH "Docs:01.3 SSH")
-   **Knowledge of terminal/bash**
    -   For an intro to basic terminal/bash commands see [00.2 Terminal Unix Commands Cheat Sheet](https://wiki4print.servpub.net/index.php?title=00.2_Terminal_Unix_Commands_Cheat_Sheet "00.2 Terminal Unix Commands Cheat Sheet")
-   **A Server with public IP (optional)**
    -   This is to hos a VPN on, but is only needed if you want to host things publically.

## Foundational / Background information (⁄ ⁄•⁄ω⁄•⁄ ⁄)

If you're new to sever-ing and sysadmin, you may find the following guides useful as they explain more of the basics of how these things work:

-   [00.1 Network terminology](https://wiki4print.servpub.net/index.php?title=Docs:00.1_Network_terminology "Docs:00.1 Network terminology")
    -   Gives an overview of terms we will be using throughout this guide in relation to networking
-   [00.2 Terminal Unix Commands Cheat Sheet](https://wiki4print.servpub.net/index.php?title=Docs:00.2_Terminal_Unix_Commands_Cheat_Sheet "Docs:00.2 Terminal Unix Commands Cheat Sheet")
    -   Is an introduction to working on the command line.

## Access (〜￣▽￣)〜

In-grid has tried to make these docs accessible and legible (as possible) to both technical and non-technical reading. We have done this through not only try to follow the [Web Content Access Guidelines](https://www.wcag.com/resource/wcag-quick-tips-for-content-writers/) but also working with the concept of *semi-plain* language that Kelsie Acton notes in here chapter *Plain Language for Disability Culture* in [Crip Authorship](https://nyupress.org/9781479819362/crip-authorship/). Acton states this as:

> Note on writing: This chapter is written in what I call a semi- plain language style. This means I do the following:
> 
> -   Use an active voice
> -   Mostly use the 6000 most common words in the English language
> -   Use short sentences
> -   Use 14 point font
> -   Use “I” and “you”

Following Acton, In-grid understands this as not trying to assimilate dialogues into dominant technical talking points, but we approach this practice through critical access to distribute and share the expertise of systems and make the disputable from many backgrounds and knowledges.

In-grid also approaches this as a place of design friction. This is where we have made room within and around these hard network infrastructures with and for our softer practices of collective access. In this space of semi-plain In-grid have iterated our own attempt at semi-plain technical docs!

We may also use "us" and "we" to state In-grid and Servpub collaborators who made this infrastructure.

If you want a light, but still deep exploration of the setup, check out the [Index of each section](https://wiki4print.servpub.net/index.php?title=Docs:00_Contents#Index_of_Sections) listed above.

If you have any access requests, please email: in-grid@in-grid.io