---
title: Smooth Auto-Replace Functionality in EmEditor, A Premier Text Editing Software
date: 2024-10-02T17:17:35.530Z
updated: 2024-10-08T17:41:11.657Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/6644f0a2d74892fa3a39d2d46d9f44395a7ca3377bb37001448c4704afb2e518.jpg
---

## Smooth Auto-Replace Functionality in EmEditor, A Premier Text Editing Software

Viewing 2 posts - 1 through 2 (of 2 total)

* Author  
Posts
* November 7, 2009 at 2:15 pm [#7796](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/6bcb99132a36c4c1b97328e2a7058784?s=80&d=identicon&r=g)WmMitchell](https://www.emeditor.com/forums/users/wmmitchell/ "View WmMitchell's profile")  
Participant  
I posted this in the regex group, which might have been a mistake. I think that it might actually be better here.  
 I’m not getting consistent results with the S&R macro below. If I don’t put:  
 document.selection.StartOfDocument(false);  
 shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
 a lot in the document to periodically force the cursor to the top of the document being edited, the macro doesn’t replace \_all\_ items, even though I have put the option eeReplaceAll in every single S&R instance. Even forcing the cursor up to the top of doesn’t make the S&R perform consistently and I have to manually invoke this script 2 or 3 times.  
 ————————————————————  
 document.selection.StartOfDocument(false);  
 shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
 document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“? “,”? “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“? “,”? “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“! “,”! “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“! “,”! “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“: “,”: “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“: “,”: “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“Dr. “,”Dr. “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“Mr. “,”Mr. “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“Mrs. “,”Mrs. “,eeFindNext | eeReplaceAll);  
 document.selection.Replace(“Lt. “,”Lt. “,eeFindNext | eeReplaceAll);  
 document.selection.StartOfDocument(false);  
 shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
 document.selection.Replace(“1/4″,”¼”,eeFindNext | eeReplaceAll);  
 document.selection.StartOfDocument(false);  
 shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
 document.selection.Replace(“1/2″,”½”,eeFindNext | eeReplaceAll);  
 document.selection.StartOfDocument(false);  
 shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
 document.selection.Replace(“3/4″,”¾”,eeFindNext | eeReplaceAll);  
 ————————————————————  
 I saw an example of a macro in what looks like an old forum for EmEditor and subsituted eeFindNext for eeFindReplaceQuiet, but that didn’t make the macro work repeatedly until all instances found and fixed.  
 What can be done to ensure the macro “loops” through each function until done, pls?  
 Thanks!  
November 8, 2009 at 6:29 pm [#7803](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
> WmMitchell wrote:  
> I posted this in the regex group, which might have been a mistake. I think that it might actually be better here.  
>  
> I’m not getting consistent results with the S&R macro below. If I don’t put:  
>  
> document.selection.StartOfDocument(false);  
> shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
>  
> a lot in the document to periodically force the cursor to the top of the document being edited, the macro doesn’t replace \_all\_ items, even though I have put the option eeReplaceAll in every single S&R instance. Even forcing the cursor up to the top of doesn’t make the S&R perform consistently and I have to manually invoke this script 2 or 3 times.  
>  
> ————————————————————  
> document.selection.StartOfDocument(false);  
> shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
>  
> document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“. “,”. “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“? “,”? “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“? “,”? “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“! “,”! “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“! “,”! “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“: “,”: “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“: “,”: “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“Dr. “,”Dr. “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“Mr. “,”Mr. “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“Mrs. “,”Mrs. “,eeFindNext | eeReplaceAll);  
> document.selection.Replace(“Lt. “,”Lt. “,eeFindNext | eeReplaceAll);  
>  
> document.selection.StartOfDocument(false);  
> shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
> document.selection.Replace(“1/4″,”¼”,eeFindNext | eeReplaceAll);  
> document.selection.StartOfDocument(false);  
> shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
> document.selection.Replace(“1/2″,”½”,eeFindNext | eeReplaceAll);  
> document.selection.StartOfDocument(false);  
> shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);  
> document.selection.Replace(“3/4″,”¾”,eeFindNext | eeReplaceAll);  
> ————————————————————  
>  
> I saw an example of a macro in what looks like an old forum for EmEditor and subsituted eeFindNext for eeFindReplaceQuiet, but that didn’t make the macro work repeatedly until all instances found and fixed.  
>  
> What can be done to ensure the macro “loops” through each function until done, pls?  
>  
> Thanks!  
 “eeFindNext | eeReplaceAll” should be enough, and you shouldn’t use shell.SendKeys(“{CTRL DOWN}{CTRL UP}”);.  
 Can you simplify your test program and a sample file, and email me at [tech@emurasoft.com](https://tools.techidaily.com/emeditor/products/) ? I will try to reproduce your problem, and fix it if it is a bug of EmEditor.  
 Thank you.
* Author  
Posts

Viewing 2 posts - 1 through 2 (of 2 total)

* You must be logged in to reply to this topic.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://instagram-video-recordings.techidaily.com/new-2024-approved-mastering-visual-storytelling-the-cutting-edge-6-instagram-reel-tools/"><u>[New] 2024 Approved Mastering Visual Storytelling The Cutting-Edge 6 Instagram Reel Tools</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/new-2024-approved-the-modern-way-tweeting-videos-to-whatsapp/"><u>[New] 2024 Approved The Modern Way Tweeting Videos to WhatsApp</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/new-strategic-sharing-of-tiktok-content-on-twitter/"><u>[New] Strategic Sharing of TikTok Content on Twitter</u></a></li>
<li><a href="https://extra-tips.techidaily.com/updated-best-storage-deals-cloud-pricing-of-future-year/"><u>[Updated] Best Storage Deals Cloud Pricing of Future Year</u></a></li>
<li><a href="https://app-tips.techidaily.com/ciq-gains-support-from-linux-experts-as-main-backer-of-rocks-cluster-os-initiative-techinsight/"><u>CIQ Gains Support From Linux Experts as Main Backer of Rocks Cluster OS Initiative - TechInsight</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/easy-update-techniques-to-optimize-your-epson-wf-7620-driver-on-pc/"><u>Easy Update Techniques to Optimize Your Epson WF-7620 Driver on PC</u></a></li>
<li><a href="https://techidaily.com/how-to-easily-hard-reset-my-vivo-v30-drfone-by-drfone-reset-android-reset-android/"><u>How to Easily Hard reset my Vivo V30 | Dr.fone</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-best-motorola-moto-g13-pattern-lock-removal-tools-remove-android-pattern-lock-without-losing-data-by-drfone-android/"><u>In 2024, Best Motorola Moto G13 Pattern Lock Removal Tools Remove Android Pattern Lock Without Losing Data</u></a></li>
<li><a href="https://win-help.techidaily.com/step-by-step-guide-downloading-usa-today-news-videos-from-pc-or-mac/"><u>Step-by-Step Guide: Downloading 'USA Today' News Videos From PC or Mac</u></a></li>
<li><a href="https://win-help.techidaily.com/step-by-step-guide-downloading-videos-from-vkonto-apps-on-pc-or-mac/"><u>Step-by-Step Guide: Downloading Videos From VKonto Apps on PC or MAC</u></a></li>
<li><a href="https://win-help.techidaily.com/the-ultimate-guide-to-top-5-highest-ranked-video-downloading-tools-for-macos-and-windows-users/"><u>The Ultimate Guide to Top 5 Highest-Ranked Video Downloading Tools for macOS & Windows Users</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/top-chatbot-solutions-that-outshine-chatgpt-a-comprehensive-list/"><u>Top Chatbot Solutions That Outshine ChatGPT: A Comprehensive List</u></a></li>
<li><a href="https://win-help.techidaily.com/top-ranking-mp3-converter-software-compared-allavsoft-vs-others/"><u>Top-Ranking MP3 Converter Software Compared: Allavsoft vs Others</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135407/19272" target="_top" id="2135407">
  <img src="//a.impactradius-go.com/display-ad/19272-2135407" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135407/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

