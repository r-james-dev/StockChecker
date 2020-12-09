## Stock Checker

This stock checker is dedicated specifically to <code>Nvidia 30 Series GPUs</code>, <code>AMD 6000 Series GPUs</code> and <code>AMD 5000 Series CPUs</code> but it can be used for other products also. It comes with some common **United Kingdom** stores built in the <a href="stores.json">stores.json</a> file.

## Quick start

Stock Checker runs on Python 3.X.X:

```shell
git clone https://github.com/conorvenus/StockChecker
cd StockChecker
py main.py
```

## Customisation

⚠️ Customising this Stock Checker is primarily targeted at experienced programmers who understand the json file format.

Open the <a href="stores.json">stores.json</a> file and add a new store object to the array:

### Structure of the Store Object

```json
{
  "name": "e.g. newegg",
  "url": "https://www.newegg.com/p/pl?d=RTX+3060+Ti",
  "method": "e.g. selenium",
  "card_name": "e.g. 3060 ti",
  "country": "us",
  "webscraping": {
    "product": {
      "type": "",
      "data_type": "",
      "class": ""
    },
    "title": {
      "type": "",
      "data_type": "",
      "data-product": ""
    },
    "url": {
      "type": "",
      "data_type": "",
      "class": "",
      "append_base_url": false
    },
    "stock_identifier": {
      "type": "",
      "data_type": "",
      "class": "",
      "outofstock": true
    }
  }
}
```

<details>
<summary>Normal Options</summary>
<table>
<thead>
<tr>
<th align="center">Key</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><code>name</code></td>
<td>Name of store you're using, this is just for logging purposes for a good UX.</td>
</tr>
<tr>
<td align="center"><code>url</code></td>
<td>URL of the store product search, should be a page with a list of all references of that product on.</td>
</tr>
<tr>
<td align="center"><code>method</code></td>
<td>selenium/request</td>
</tr>
<tr>
<td align="center"><code>card_name</code></td>
<td>This is used to confirm that you're scraping the right product each time.</td>
</tr>
<tr>
<td align="center"><code>country</code></td>
<td>Specify a country, stick to a specific format, e.g. us/uk, <code>optional</code> key!</td>
</tbody>
</table>
</summary>
</details>

<details>
<summary>Web Scraping Options</summary>
<table>
<thead>
<tr>
<th align="center">Object Name</th>
<th>Key</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><code>product</code></td>
<td>type</td>
<td>The <code>tag</code> of the html element that corresponds to each product.<br>__e.g. div__</td>
</tr>
<tr>
<td align="center"><code>product</code></td>
<td>data_type</td>
<td>The <code>attribute</code> of the html element that corresponds to each product.<br>__e.g. class__</td>
</tr>
<tr>
<td align="center"><code>product</code></td>
<td>value from <code>data_type</code></td>
<td>The <code>actual value given to the attribute</code> of the html element that corresponds to each product.<br>__e.g. product-listing__</td>
</tr>
</tbody>
</table>
</summary>
</details>
