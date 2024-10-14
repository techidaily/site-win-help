---
title: Smooth Auto-Replace Functionality in EmEditor, A Premier Text Editing Software
date: 2024-10-09T16:15:59.505Z
updated: 2024-10-14T16:00:12.387Z
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
<li><a href="https://facebook-video-footage.techidaily.com/new-champion-toolkit-10-budget-friendly-caption-extractors-for-2024/"><u>[New] Champion Toolkit 10 Budget-Friendly Caption Extractors for 2024</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/approved-freely-accessible-cutting-edge-video-editor-tools/"><u>2024 Approved Freely Accessible Cutting Edge Video Editor Tools</u></a></li>
<li><a href="https://win-help.techidaily.com/amazingly-odd-phenomenon-when-deleting-files-understanding-emeditors-behavior/"><u>Amazingly Odd Phenomenon When Deleting Files - Understanding EmEditor's Behavior</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/efficient-file-conversion-convert-mov-to-mp4-avi-or-flv-using-the-best-compressor-tools/"><u>Efficient File Conversion: Convert MOV to MP4, AVI, or FLV Using the Best Compressor Tools</u></a></li>
<li><a href="https://win-help.techidaily.com/emeditor-text-editor-enhance-your-search-with-quick-find-across-documents/"><u>EmEditor Text Editor: Enhance Your Search with Quick Find Across Documents</u></a></li>
<li><a href="https://win11-tips.techidaily.com/from-red-to-ready-8-methods-to-mend-your-monochrome-misstep/"><u>From Red to Ready: 8 Methods to Mend Your Monochrome Misstep</u></a></li>
<li><a href="https://win-help.techidaily.com/how-to-perform-find-and-replace-in-emeditor-adjusting-column-or-row-settings-for-text-editing/"><u>How to Perform Find and Replace in EmEditor - Adjusting Column or Row Settings for Text Editing</u></a></li>
<li><a href="https://win-help.techidaily.com/how-to-use-emeditors-reply-feature-in-a-bookmarked-thread/"><u>How to Use EmEditor's Reply Feature in a Bookmarked Thread</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/in-2024-9-mind-blowing-tricks-to-hatch-eggs-in-pokemon-go-without-walking-on-xiaomi-redmi-k70-drfone-by-drfone-virtual-android/"><u>In 2024, 9 Mind-Blowing Tricks to Hatch Eggs in Pokemon Go Without Walking On Xiaomi Redmi K70 | Dr.fone</u></a></li>
<li><a href="https://some-techniques.techidaily.com/in-2024-harmonizing-history-best-theme-songs-in-anime/"><u>In 2024, Harmonizing History Best Theme Songs in Anime</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/laughter-lab-virtually/"><u>Laughter Lab Virtually</u></a></li>
<li><a href="https://win-help.techidaily.com/mark-selections-using-space-tabs-end-of-line-method-for-improved-editing-in-emeditor/"><u>Mark Selections Using Space Tabs End-of-Line Method for Improved Editing in EmEditor</u></a></li>
<li><a href="https://discover-advanced.techidaily.com/optimized-with-cookiebot-revolutionizing-digital-strategies-in-seo-and-analytics/"><u>Optimized with Cookiebot: Revolutionizing Digital Strategies in SEO and Analytics</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/1722517232141-outdated-or-optimal-for-your-online-needs-a-thorough-review-of-the-netgear-c3-grower-style-router/"><u>Outdated or Optimal for Your Online Needs? A Thorough Review of the Netgear C3 Grower-Style Router</u></a></li>
<li><a href="https://win-help.techidaily.com/setting-up-custom-hotkeys-in-emeditor-for-quick-access-to-plugin-functions/"><u>Setting Up Custom Hotkeys in EmEditor for Quick Access to Plugin Functions</u></a></li>
<li><a href="https://win-help.techidaily.com/troubleshooting-the-replytoquerystatusbyid-feature-in-emeditor-eeidfindbarincremental-issue-45/"><u>Troubleshooting the ReplyTo:QueryStatusByID Feature in EmEditor - EEID_FINDBAR_INCREMENTAL Issue (45^)</u></a></li>
<li><a href="https://win-help.techidaily.com/understanding-emeditors-data-protection-a-guide-to-its-automatic-backup-capability/"><u>Understanding EmEditor's Data Protection: A Guide to Its Automatic Backup Capability</u></a></li>
<li><a href="https://win-help.techidaily.com/understanding-finalization-scripts-with-emeditor-insights-into-a-powerful-text-processors-capabilities/"><u>Understanding Finalization Scripts with EmEditor: Insights Into a Powerful Text Processor's Capabilities</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/unveiling-social-screens-share-your-monitor-on-fb-live/"><u>Unveiling Social Screens Share Your Monitor on FB Live</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://coinrule.sjv.io/c/5597632/1610918/18409" target="_top" id="1610918">
  <img src="//a.impactradius-go.com/display-ad/18409-1610918" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://coinrule.sjv.io/i/5597632/1610918/18409" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

