
Problem - Convert the characters &, <, >, " (double quote), and ' (apostrophe), in a string to their corresponding HTML entities.

```
function convertHTML(str) {
  const regex = /[&<>"']/gi;
  const hasMatch = regex.test(str);
  str = str.replace(regex, replacer);  
  return str;
}

function replacer(match) {
  const entityLookup = {
    '&' : '&amp;',
    '<' : '&lt;',
    '>' : '&gt;',
    '"': '&quot;',
    "'": '&apos;'
  }
  return entityLookup[match];  
}

convertHTML("Dolce & Gabbana");
convertHTML("Hamburgers < Pizza < Tacos")

```
