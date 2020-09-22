<div align="center">

## Javascript Ticker


</div>

### Description

This is a neat little script written in javascript that acts like a newsticker. Each message also displays as a link, so you can click on the link to go to tht page. This is based off of one of Premshree Pillai's javascripts.
 
### More Info
 
Orginal author: Premshree Pillai

Modifications by: darocker22


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[darocker22](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/darocker22.md)
**Level**          |Intermediate
**User Rating**    |4.3 (17 globes from 4 users)
**Compatibility**  |
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/darocker22-javascript-ticker__2-2658/archive/master.zip)





### Source Code

```
<html>
<HEAD>
<SCRIPT LANGUAGE="JavaScript">
<!-- Begin
window.onerror = null;
 var bName = navigator.appName;
 var bVer = parseInt(navigator.appVersion);
 var NS4 = (bName == "Netscape" && bVer >= 4);
 var IE4 = (bName == "Microsoft Internet Explorer"
 && bVer >= 4);
 var NS3 = (bName == "Netscape" && bVer < 4);
 var IE3 = (bName == "Microsoft Internet Explorer"
 && bVer < 4);
 var i=0;
// Change the position of the ticker
 var top_pos = 275;
 var left_pos = 200;
// Change the speed of the ticker (in milliseconds)
 var time_length = 2000;
 var div_name = "qiksearch";
// Enter messages for the ticker
 var ticker_msg = new Array(
  "Welcome to Planet-Source-Code.com",
  "Visual Basic World",
  "Java/JavaScript World",
  "C / C++ World",
  "ASP/VbScript World",
  "SQL World",
  "Perl World",
  "Delphi World",
  "PHP World",
  "Cold Fusion World",
  ".Net World",
  "Check out RentACoder.com" );
// Enter the URL's for the above messages
 var ticker_url = new Array(
  "http://www.planet-source-code.com/",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=1",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=2",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=3",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=4",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=5",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=6",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=7",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=8",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=9",
  "http://www.planet-source-code.com/vb/default.asp?lngWId=10",
  "http://www.rentacoder.com" );
var ticker_len = ticker_msg.length;
for(var l=0; l<ticker_len; l++)
{
 document.write('<div id="' + div_name + l + '" style="position:absolute; visibility:hidden; top:' + top_pos + '; left:' + left_pos + '">' + '<table bgcolor="#000000" cellspacing="0" cellpadding="1" width="400"><tr><td><table width="100%" bgcolor="#EFEFEF"><tr><td><center><a href="' + ticker_url[l] + '" class="tick">' + ticker_msg[l] + '</center></a></td>');
 document.write('</tr></table></td></tr></table>' + '</div>');
}
if (NS4 || IE4)
{
 if (navigator.appName == "Netscape")
 {
  layerStyleRef="layer.";
  layerRef="document.layers";
  styleSwitch="";
 }
 else
 {
  layerStyleRef="layer.style.";
  layerRef="document.all";
  styleSwitch=".style";
 }
}
//SCROLL
function tick(){
if (NS4 || IE4)
{
 if(i<ticker_len)
 {
  if(i==0)
  {
  eval(layerRef+'["'+div_name+(ticker_len-1)+'"]'+
  styleSwitch+'.visibility="hidden"');
  }
  if(i>0)
  {
  eval(layerRef+'["'+div_name+(i-1)+'"]'+
  styleSwitch+'.visibility="hidden"');
  }
  eval(layerRef+'["'+div_name+i+'"]'+
  styleSwitch+'.visibility="visible"');
 }
 if(i<ticker_len-1)
 {
 i++;
 }
 else
 {
 i=0;
 }
 setTimeout("tick()",time_length);
 }
}
tick();
// End -->
</script>
</body>
</html>
```

