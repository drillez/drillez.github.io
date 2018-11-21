---
layout: "post"
title: "Reflektion"
---

<h4>What do you think of pre-compiling your CSS?</h4>

<ul>
<li>Compare to regular CSS</li>
<li>Which techniques did you use?</li>
<li>Pros and cons?</li>
</ul>
När jag började med denna uppgift i detta fall modifera en hemsida med Jekyll och pre-comiling CSS så kändes det ganska svårt. Ju mer man kollade på koden ju mer "lost" blev man. Efter har kollat på en massa tutorials på youtube om Jekyll och pre-CSS så började man förstå en del och det som kändes svårt i början började bli lite enklare nu. När jag väl började förstå så blev det även lite roligare att jobba med Jekyll och pre-compiling CSS. Har dock inte gjort så mycket förändringar än. Om man jämför pre-compling CSS med CSS så tycker jag än så länge att den CSS kod man jobbade med Webbtekniken känns enklare, men som sagt än så länge bara för tror när man lär sig mer om pre-compling CSS så kommer det bli enklare, smidigare och roligare.

 Då jag inte har kommit så långt med hemsidan än så jag har jag inte hunnit använda mig av några speciella tekniker.

För/nackdelar.
Av den lilla erfarenheten jag har fått med att jobba med pre-compiling så tycker jag att det är ett bra sätt att jobba på om man nu vill bygga en stor hemsida. Vill man tex ha en schysst layuout på alla sina sidor med en header eller något annat, vill man sedan ändra på det så är ju det väldigt enkelt att göra. Så istället att byta på massa olika filer så kan man med pre-compiling byta på ett ställe och det ändras på alla sidor. Till skillnad på vanlig CSS där man kanske får lägga ner tid och byta på alla sidor. 
En nackdel med att jobba med pre-compiling kan ju va om man nu vill börja ett stort projekt där du inte jobbar ensam utan att man jobbar med massa andra. Då är det ju ganska viktigt att alla kan/vet hur man  jobbar med pre-CSS annars kan det orsaka stora problem om man börja ändra på kod som man inte förstår.

<h4>What do you think of static site generators?</h4>
<ul>
<li>What type of projects are they suitable for?</li>
</ul>

Fördelarna med att köra static site generators är att först och främst så går det snabbare för sidan att laddas upp då blir färre anrop till servern, den blir mycket säkrare och även billigare att använda.
Med detta sagt så tyker jag att det är bra att köra med static site generators. 
Static site generators är passande för tex bloggar, dokumentation och informationssidor.

<h4>What is robots.txt and how have you configure it for your site?</h4>

robots.txt är en text-fil som sökmotorer och så kallade robotar hämtar för att kontrollera vilka mappar och filer dom får åtkomst till. Man kan själv styra om man vill att dom ska få tillgång till dessa mappar/filer eller välja att istället blockera dom.
Jag gjorde det enkelt och valde att blockera för detta. Koden jag använder mig utav är,
{% highlight ruby %}
User-agent: *
Disallow: /
{% endhighlight %}

<h4>What is humans.txt and how have you configure it for your site?</h4>

human.txt är en enkel text-fil som innehåller information om vem/vilka som byggt webbplatsen. Man kan givetvis lägga till vilken information man vill som är relevant för webbplatsen. I min text-fil så har jag lagt till detta.
{% highlight ruby %}
Dritan Zendeli
Email: dz222bi@lnu.Sweden
Github: Drillez
Twitter: Har ingen
Location: Kalmar, Sweden
{% endhighlight %}

<h4>How did you implements comments to blog posts</h4>

Jag körde på att anvävda disqus vilket va rekomenderat. Kändes som att det skulle vara svårt att lägga till disqus men när man väl registrerade sig på sidan så fick man en väldig enkel förklaring till hur man ska installera allt. Först försökte jag använda mig utav plattformen Jekyll men det funkade inte så bra så bytte till universal code. Nedan ser ni koden jag implenterade i post.html enligt instuktionerna.
{% highlight ruby %}
(function() { 
var d = document, s = d.createElement('script');
s.src = 'https://https-drillez-github-io.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endhighlight %}

<h4>What is Open Graph and how do you make use of it?</h4>

I Open graph kan du lägga in information hur du vill att din webbplats presenteras när den länkas på tex sociala medier. I open graph så kan man ha en titel, bild och en beskrivning av din website. När man ska skicka länken till någon säg via sociala medier så istället för att det bara är en länk med text så får man nu ut som vi sa innan, en titel en bild och en beskrivning för din website. Ser mycket trevligare ut enligt mig själv och förmodligen tycker dom flesta likadant. Open graph läggs in i meta taggar i din html.head fil. Har lagt in detta i min html.head men just nu får jag bara ut title och github.io länk, försöker lägga till en bild med just nu får jag det inte att funka. 