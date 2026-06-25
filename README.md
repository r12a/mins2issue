# mins2issue
Simple web based tool to convert parts of W3C minutes output into a form that can be dropped into a github issue.  No installation needed – this is just a web page.

The output starts by listing actions raised, and resolutions taken. Then an expandable prompt can be opened to reveal the relevant section of the minutes. It's possible to also include a link to the minutes page.

Some groups use a bot to produce similar results. This tool is different in that it works from the published minutes pages – no need to issue commands during the meeting to capture the information. It seems to work ok with minutes pages produced by rrsagent (including v2) and scribejs.

I wrote this tool very quickly, so if you encounter a bug, please suggest a fix (it's very simple code).

## To use the tool:

1. Go to https://r12a.github.io/mins2issue/

2. [optional] Paste the URL of the minutes page into the box with the label `URL of meeting minutes`.

3. Select the lines you want from the page of minutes, and copy/paste them into the large box on the left.

4. Click on `Generate issue comment`.

5. Copy the highlighted result from the right-hand box, and paste it into a comment box in a GitHub issue.


## Example

### The following extract from a minutes page:
```
<scribe> fantasai: Two issues are rejected
... https://drafts.csswg.org/css-text-decor-3/issues-cr-2013#issue-14
... A request to forbid text emphasis from having only a color.
... We already allow this for border, etc.
<Zakim> q+ tantek
<scribe> astearns: Have they responded to rejection?
<scribe> fantasai: I think he's ok with it but haven't found email.
<scribe> tantek: I'm missing why we should do this.
... Border color is right answer, we already have this pattern.
RESOLVED: We reject issue 14 but will follow up.
<scribe> fantasai: tab followed up, there was no response for a year
<tantek> tab's message URL?
<tantek>(was not linked from Xidorn's message)
<fantasai> https://lists.w3.org/Archives/Public/www-style/2015Nov/0355.html
<scribe> fantasai: because our archive software is terrible
<Zakim> ack tantek
<scribe> tantek: agreed resolve per Tab's response / explanation
<scribe> ACTION: Fantasai to contact Xidorn about issue #14
<trackbot> Created ACTION-14 - contact Xidorn about issue #14 [on Fantasai - due 2017-08-17].
```

### will be converted to text that will look like this when dropped into an issue comment field:


This issue was discussed in [a meeting](https://lists.w3.org/Archives/Public/www-style/2017Feb/0049.html).

<p>- RESOLVED:  We reject issue 14 but will follow up.</p>- ACTION: contact Xidorn about issue #14 [on Fantasai - due 2017-08-17].</p><details open><summary><i class="differentiate">View the transcript</i></summary>
<b>fantasai:</b> Two issues are rejected<br/>
... <a href="https://drafts.csswg.org/css-text-decor-3/issues-cr-2013#issue-14">https://drafts.csswg.org/css-text-decor-3/issues-cr-2013#issue-14</a><br/>
... A request to forbid text emphasis from having only a color.<br/>
... We already allow this for border, etc.<br/>
<b>astearns:</b> Have they responded to rejection?<br/>
<b>fantasai:</b> I think he's ok with it but haven't found email.<br/>
<b>tantek:</b> I'm missing why we should do this.<br/>
... Border color is right answer, we already have this pattern.<br/>
<b>RESOLVED:</b> We reject issue 14 but will follow up.<br/>
<b>fantasai:</b> tab followed up, there was no response for a year<br/>
<b>&lt;tantek&gt;</b> tab's message URL?<br/>
<b>&lt;tantek&gt;</b>(was not linked from Xidorn's message)<br/>
<b>fantasai:</b> because our archive software is terrible<br/>
<b>tantek:</b> agreed resolve per Tab's response / explanation<br/>
<b>ACTION:</b> Fantasai to contact Xidorn about issue #14<br/>
<b>&lt;trackbot&gt;</b> Created ACTION-14 - contact Xidorn about issue #14 [on Fantasai - due 2017-08-17].<br/>
</details>


### it also produces a quick view in HTML that looks like this:


<img width="1416" height="784" alt="Screenshot 2026-06-25 at 11 01 38" src="https://github.com/user-attachments/assets/0b3f9621-a5b5-4f8a-a866-23dd8876101c" />
