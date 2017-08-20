# Tindie label print
An stupidly simple label printer template for continuous label printers (e.g. Brother QL-series).

The idea is beyond trivial: it is an HTML page that takes `from` and `to` as query string parameters and formats them into a label template that is ready to be sent directly to a label printer.

## What do I need?
You will need a label printer and some continuous paper label roll. I am using the following:
 * [Brother QL-570 Label Printer](http://support.brother.com/g/b/spec.aspx?c=eu_ot&lang=en&prod=lpql570euk)
 * [DK-44205 Continuous Paper Label Roll, 62mm](https://www.brother.co.uk/supplies/label-printers/labels/dk/copy-of-dk44205)

## How to use?
The easiest way to use is to create a [bookmarklet](https://en.wikipedia.org/wiki/Bookmarklet) to invoke this directly from a Tindie order page.

Create a new bookmark with the following URL (replacing the `YOUR XXX` placeholders with your own address details):
```
  javascript:window.location.href='http://gnz.io/tindie-label-print?from=' + encodeURIComponent(['YOUR NAME', 'YOUR STREET', 'YOUR ZIP/CITY', 'YOUR COUNTRY'].join('__')) + '&to=' + encodeURIComponent(document.querySelector('address').innerText.split('\n').join('__'))
```

Then, go to your store in Tindie, open any of your unshipped orders, and click your newly created bookmarklet! If the printer is configured, the print dialog will pop up automatically, and you can send the job right away.

## Will it work with my printer?
Probably not. Or yes. Who knows. The template is so simplistic that I guess it only works for my very specific setup, but feel free to send a pull request to improve it, or fork it and do your own. 

## Why did you do it?
Because I sell some stuff on [tindie.com](https://www.tindie.com) and I was tired of writting down addresses all the time.

# License
This fantastically complex piece of code is made available under an [MIT license](LICENSE).

