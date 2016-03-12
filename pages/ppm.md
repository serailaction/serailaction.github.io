---
layout: page
category : 
tagline: since the direct award
title: PPM historical data
tags : 
comments: true
summary: 
---

{% include JB/setup %}


This is some text for a post
asdf


<div id="ppmtable">replace me</div>

<script src="data.js"></script>
<script>
function loadTable(){
    out='<table>'
    out+='<tr><td>Line of route</td>'
    ppms=[]
    for (x in json_ppm){
        ppms.push(x)
    }
    ppms.sort()
    for (x in ppms){
        out+='<td colspan="2">'+ppms[x]+'</td>'
    }
    for (x in ppms){
        a='Target'
    
    }
    out+='</tr>'
    out+='</table>'
    document.getElementById("ppmtable").innerHTML=out
}
</script>


<script>loadTable()</script>