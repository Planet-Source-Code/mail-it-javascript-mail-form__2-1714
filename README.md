<div align="center">

## Mail It \(JavaScript Mail Form\)


</div>

### Description

Andy Augustine

Description: You can use standard HTML to send email to a "hard-coded" email address with a "hard-coded" subject. (The body of the message can be any info keyed in the form). However, if you want to send email to a user-specified email address and/or a user-specified subject, then HTML cannot do the job. This script shows how Javascript can be used to allow the user of the form to specify the recipient and subject (the trick: use a hidden form and populate this form with the contents of the visible form). You can customise the visible form to suit your requirements. Please note that if you have not configured your browser's email program, this script will not work.
 
### More Info
 
Instructions

1. Copy Part 1 into the HEAD section of your HTML document.

2. Copy Part 2 into the BODY section of your HTML Document.

3. Customize the form.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[N/A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/empty.md)
**Level**          |Unknown
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/mail-it-javascript-mail-form__2-1714/archive/master.zip)





### Source Code

```
<html>
<!-----------------------------------------JavaScript Mail Form by Andy AugustineJavaScript archived by the JavaScript Cornerhttp://pbc.bh1com.com------------------------------------------>
<head>
<script Language="JavaScript">
<!-- this is not part of the javascript demo - plz ignore it
if (window.focus) { self.focus();}
//-->
</script>
<title>JavaScript Mail Form</title>
<!------------------------------------------########## Script Part 1 ###################Copy this part into the HEAD of your page------------------------------------------->
<script Language="JavaScript">
<!-- hide script from non compliant broswers
/* Author's Name:	 Andy Augustine
JavaScript Snippet:	 'mailIt'
E-mail address:	 jspro@nquiry.com
Original Location:	 http://www.inquiry.com/techtips/js_pro/
	Permission granted to freely distribute	and use	this
	code as	long as	this header remains in tact.
		 (c)1996 Andy Augustine				  */
//modified by Pete Bof: 1. humanized email: change enctype to text/plain
//           2. customised email body
function mailIt(form) {
var data = document.dataForm
var userInfo = ""
// comment out the next line if you want to hardcode the reciepient
// then add 'foo@ar.com' to the 'mailform' action attribute
// (i.e. -- ACTION="mailto:foo@ar.com")
form.action += data.recipient.value
// comment out the next line if you want to hardcode the subject
// then add '?subject=example' to the	'mailform' action attribute.
// You must hardcode an address before you can hardcode a subject.
// (i.e. -- ACTION="mailto:foo@bar.com?subject=example")
form.action += "?subject=" + data.subject.value
userInfo += "Page Title: " +	document.title + "\n"
userInfo += "Mailed From: " +	document.location + "\n\n"
form.mailBody.value =	userInfo + "\n"+data.name.value +"\n"
+ data.country.value + "\n" +"\n"+ data.email.value
+ "\n"+data.rating.value
return true
}
// -->
// end hiding from non compliant browsers-->
</script>
<!------------------------------------------########## End of Script Part 1 ############------------------------------------------->
</head>
<body>
<p align="center"><img src="../../bitmaps/demo.gif" WIDTH="480" HEIGHT="43"></p>
<center><p>
<font size="3" face="Verdana, Helvetica, Arial , sans-serif"><strong>
JavaScript Mail Form
</strong></b>
</p></center>
<p>
<font size="2" face="Verdana, Helvetica, Arial , sans-serif">
You can use standard HTML to send email to a "hard-coded" email address
with a "hard-coded" subject. (The body of the message can be any info keyed in the form).
However, if you want to send email to a user-specified email address and/or a user-specified
subject, then HTML cannot do the job. This script shows how Javascript can be used to allow
the user of the form to specify the recipient and subject (the trick: use a hidden form
and populate this form with the contents of the visible form). You can customise the visible
form to suit your requirements. Please note that if you have not configured your browser's
email program, this script will not work. <br><br>
Try it! send an email to us with your rating. Then, send an email to yourself and see how the
email message looks like.
</font>
</p>
<!------------------------------------------########## Script Part 3 ###################Copy Part 2 into the BODY section of your HTML Document------------------------------------------->
<font size="3">Rate us</font>
<table>
<form NAME="dataForm">
<!-- DELETE THIS TABLE ROW IF YOU'RE HARDCODING	A RECIPIENT -->
<tr>
<th ALIGN="right">Recipient:
<td><input NAME="recipient" SIZE="40" VALUE="pbc@pbc.bhcom1.com">
</tr>
<!-- DELETE THIS TABLE	ROW IF YOU'RE HARDCODING A SUBJECT -->
<tr>
<th ALIGN="right">Subject:
<td><input NAME="subject" SIZE="40" VALUE="Rating of the JavaScript Corner">
</tr>
<tr>
<th ALIGN="right" VALIGN="top">Your Name:
<td><input NAME="name" SIZE="40" VALUE>
</tr>
<tr>
<th ALIGN="right" VALIGN="top">Country:
<td><input NAME="country" SIZE="40" VALUE>
</tr>
<tr>
<th ALIGN="right" VALIGN="top">eMail:
<td><input NAME="email" SIZE="40" VALUE>
</tr>
<tr>
<th ALIGN="right" VALIGN="top">How do you rate us? (1 to 10)
<td><input NAME="rating" SIZE="2" VALUE>
</tr>
</form>
</table>
<form NAME="mailForm" ACTION="mailto:" METHOD="post" ENCTYPE="text/plain" onSubmit="return mailIt(this)">
<input TYPE="hidden" NAME="mailBody" VALUE>
<tr>
<td COLSPAN="2" ALIGN="center">
<input TYPE="submit" VALUE="Send This eMail	Form Now">
</tr>
</form>
<!------------------------------------------########## End of Script Part 2 ############------------------------------------------->
</body>
</html>
```

