# JavaScript Assincrono
<p>Assícrono : Que não ocorre ou não efetiva ao mesmo tempo</p>
<p>O Javascript por padrão roda de maneira síncrona</p>
<br>
<h2>Promises</h2>
<p>É um objeto de processamento assíncrono.Inicialmente seu valor é desconheciodo.Ela pode então, ser <b>resolvida</b> ou <b>rejeitada</b></p>
<p>Uma promise tem 3 estados:</p>
<p>1 - Pending(Pendente)</p>
<p>2 - Fulfilled(Completado)</p>
<p>3 - Rejected(Deu errado)</p>
<br>
<h2>Estrutura</h2>
<p>const myPromise((resolve, rejected) =>{</p>
<p>     window.setRimeout(() => {</p>
<p>         resolve(console.log('Resolvida!'));</p>
<p>      }.2000);</p>
<p>});</p>
<p></p>
<p>await myPromise</p>
<p>           .then((result) +> result + ' passando pelo then')</p>
<p>           .then((result) +> result + ' e afora acabou!')</p>
<p>           .catch((err) => console.log(err.message));</p>
<h2>Async/await</h2>
<p>Funções assicronas precisam dessas duas palavras</p>
<p>async function resolvePromise(){</p>
<p>     const myPromise = new Promise((resolve, rejected) => {</p>
<p>         window.setTimeour(() =>{</p>
<p>             resolve('Resolvida');</p>
<p>         }, 3000);</p>
<p>});</p>
<p>     const resolved = await myPromise</p>
<p>           .then((result) +> result + ' passando pelo then')</p>
<p>           .then((result) +> result + ' e afora acabou!')</p>
<p>           .catch((err) => console.log(err.message));</p>
<p>return resolved;</p>
<p>}</p>
<p></p>
<p>Funções assincronas também retornam promises</p>
<h1>Consumindo APIs</h2>
<p>Application Programming Interface</p>
<p>Uma API é uma forma de intermediar resultados do back-end com o que é apresentado no front-end.</p>
<p>Você consegue acess-las por meio de URLs</p>
<p>JSON: Javascript Object Notation</p>
<p> É muito comum que APIs retornem seus dados no formato .json, portanto precisamos tratar esses dados quando os recebermos</p>
<br>
<h3>Método fetch()</h3>
<p>fetch(url, options)</p>
<p>     .then(response => response.json())</p>
<p>     .then(json => console.log(json))</p>
<p></p>
<p>Operações no banco(POST,GET,PUT,DELETE,etc)</p>
