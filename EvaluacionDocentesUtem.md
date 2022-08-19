Hubo un punto que a todos los profesores les puse un 7 en ciertas cosas. Para hacer el proceso más rapido cree este pequeño codigo que te pregunta la nota que deseas colocar:

Solo pegalo en la consola de JS y sigue las instrucciones (Automaticamente presiona el boton siguiente al terminar.)
```js
document.paso = document.querySelectorAll('.bwizard-steps')[0].querySelectorAll('li[class="active"]')[0].querySelectorAll('span')[0].innerText;if(confirm('Es tipo Si/No?')){ let si = prompt('Si o No?') || ''; if(si.toLowerCase() === 'si'){ document.getElementById('step'+document.paso).querySelectorAll('tbody')[0].querySelectorAll('tr').forEach(el => el.childNodes[3].querySelectorAll('input')[0].click()); } else { document.getElementById('step'+document.paso).querySelectorAll('tbody')[0].querySelectorAll('tr').forEach(el => el.childNodes[5].querySelectorAll('input')[0].click()); }} else { let ask = prompt('Nota? 1-7') || '1';let nota = (Number.parseInt(ask) * 2) + 1;document.getElementById('step'+document.paso).querySelectorAll('tbody')[0].querySelectorAll('tr').forEach(el => el.childNodes[nota].querySelectorAll('input')[0].click()); } document.querySelectorAll('.next')[0].click();
```
