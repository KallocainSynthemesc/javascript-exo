<template>
  <div class="slide">
    <div class="heading">Loop + function exercise - Caesar's cipher</div>
    <div class="content">
      <p>
        Jules César protégeait ses informations confidentielles en les chiffrant
        à l'aide d'un code. Le chiffrement de César décale chaque lettre d'un
        certain nombre de lettres. Si le décalage vous amène à dépasser la fin
        de l'alphabet, il suffit de faire une rotation vers le début de
        l'alphabet. Dans le cas d'une rotation par 3, w, x, y et z deviennent z,
        a, b et c.
        <b
          >Vous pouvez utiliser les chaînes de caractères comme des tableaux
          !</b
        >
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
                  word <span style="color: #333333">=</span> <span style="background-color: #fff0f0">&quot;magnétoplasmadynamique&quot;</span>
                  output word[<span style="color: #0000DD; font-weight: bold">0</span>] <span style="color: #888888">//m</span></pre>
      </div>

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
                  Exemple : magnétoplasmadynamique
                  Résultat <span style="color: #333333">+</span><span style="color: #0000DD; font-weight: bold">3</span> : pdjqwrsodvpdgbqdpltxh</pre>
      </div>
      <p>
        <b>Départ en avant pour ne pas avoir à créer un tableau d'alphabet</b>
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
                  <span style="color: #008800; font-weight: bold">let</span> alphabet <span style="color: #333333">=</span> [<span style="background-color: #fff0f0">&#39;a&#39;</span>,<span style="background-color: #fff0f0">&#39;b&#39;</span>,<span style="background-color: #fff0f0">&#39;c&#39;</span>,<span style="background-color: #fff0f0">&#39;d&#39;</span>,<span style="background-color: #fff0f0">&#39;e&#39;</span>,<span style="background-color: #fff0f0">&#39;f&#39;</span>,<span style="background-color: #fff0f0">&#39;g&#39;</span>,<span style="background-color: #fff0f0">&#39;h&#39;</span>,<span style="background-color: #fff0f0">&#39;i&#39;</span>,<span style="background-color: #fff0f0">&#39;j&#39;</span>,<span style="background-color: #fff0f0">&#39;k&#39;</span>,<span style="background-color: #fff0f0">&#39;l&#39;</span>,<span style="background-color: #fff0f0">&#39;m&#39;</span>,<span style="background-color: #fff0f0">&#39;n&#39;</span>,<span style="background-color: #fff0f0">&#39;o&#39;</span>,<span style="background-color: #fff0f0">&#39;p&#39;</span>,<span style="background-color: #fff0f0">&#39;q&#39;</span>,<span style="background-color: #fff0f0">&#39;r&#39;</span>,<span style="background-color: #fff0f0">&#39;s&#39;</span>,<span style="background-color: #fff0f0">&#39;t&#39;</span>,<span style="background-color: #fff0f0">&#39;u&#39;</span>,<span style="background-color: #fff0f0">&#39;v&#39;</span>,<span style="background-color: #fff0f0">&#39;w&#39;</span>,<span style="background-color: #fff0f0">&#39;x&#39;</span>,<span style="background-color: #fff0f0">&#39;y&#39;</span>,<span style="background-color: #fff0f0">&#39;z&#39;</span>]
                  <span style="color: #008800; font-weight: bold">let</span> word <span style="color: #333333">=</span> <span style="background-color: #fff0f0">&quot;magnétoplasmadynamique&quot;</span>
                  <span style="color: #008800; font-weight: bold">let</span> cesarWord <span style="color: #333333">=</span> <span style="background-color: #fff0f0">&quot;&quot;</span>
                  <span style="color: #008800; font-weight: bold">let</span> shiftNumber <span style="color: #333333">=</span> <span style="color: #007020">parseInt</span>(prompt(),<span style="color: #0000DD; font-weight: bold">10</span>);</pre>
      </div>
    </div>
  </div>
</template>
