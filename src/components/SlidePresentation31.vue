<template>
  <div class="slide">
    <div class="heading">Loop + function exercise - FizzBuzz extended</div>
    <div class="content">
      <p>
        J'ai étendu notre programme FizzBuzz pour imprimer "Fuzz" pour les
        multiples de sept et "Bizz" pour les multiples de onze. Nous répétons
        sans cesse des instructions très similaires. Ce n'est pas un bon style
        de programmation et il faut absolument le remanier. Pouvez-vous extraire
        le contrôle <b>if</b> (par exemple :
        <span style="color: #000080; font-weight: bold">if</span> ((i %
        <span style="color: #0000ff">3</span>)===<span style="color: #0000ff"
          >0</span
        >) { output += <span style="color: #0000ff">&#39;Fizz&#39;</span>; })
        dans une fonction et l'appeler simplement dans notre boucle ?
      </p>
      <div
        style="
          background: #ffffff;
          overflow: auto;
          width: auto;
          border: solid gray;
          border-width: 0.1em 0.1em 0.1em 0.8em;
          padding: 0.2em 0.6em;
        "
      >
        <pre style="margin: 0; line-height: 125%">
                  <span style="color: #000080; font-weight: bold">var</span> fizzBuzz = <span style="color: #000080; font-weight: bold">function</span> () {
                    <span style="color: #000080; font-weight: bold">var</span> i, output;
                    <span style="color: #000080; font-weight: bold">for</span> (i = <span style="color: #0000FF">1</span>; i &lt;= <span style="color: #0000FF">100</span>; i += <span style="color: #0000FF">1</span>) {
                      output = <span style="color: #0000FF">&#39;&#39;</span>;
                      <span style="color: #000080; font-weight: bold">if</span> ((i % <span style="color: #0000FF">3</span>)===<span style="color: #0000FF">0</span>) { output += <span style="color: #0000FF">&#39;Fizz&#39;</span>; }
                      <span style="color: #000080; font-weight: bold">if</span> ((i % <span style="color: #0000FF">5</span>) === <span style="color: #0000FF">0</span>) { output += <span style="color: #0000FF">&#39;Buzz&#39;</span>; }
                      <span style="color: #000080; font-weight: bold">if</span> ((i % <span style="color: #0000FF">7</span>) === <span style="color: #0000FF">0</span>) { output += <span style="color: #0000FF">&#39;Fuzz&#39;</span>; }
                      <span style="color: #000080; font-weight: bold">if</span> ((i % <span style="color: #0000FF">11</span>) === <span style="color: #0000FF">0</span>) { output += <span style="color: #0000FF">&#39;Bizz&#39;</span>; }
                      console.log(output || i);<span style="color: #008800; font-style: italic">//la chaîne vide est fausse, donc on court-circuite</span>
                    }
                  };

                  fizzBuzz();</pre>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
