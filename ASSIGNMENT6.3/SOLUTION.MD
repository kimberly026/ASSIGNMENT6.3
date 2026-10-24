# Assignment 6.3 — Overflow & Layout Fixing

Aim: To understand how CSS controls overflowing content using `visible`, `hidden`, `auto`, and `scroll`, create fixed-height containers, and fix a layout issue caused by overflowing content.


## 4. Understanding the four overflow values

[CSS Overflow: How to Handle Content That Won't Fit | Hari Palani posted on the topic | LinkedIn](https://images.openai.com/static-rsc-4/R1L7qaXLgzVTKlpme5_mhEEosrmJWWb51zK4vdNULf6JGmY3IikdQeZEavP017YFHINvwcuxFJLWlH1W8Ued3_-it-_5eY1U1dDzVv-HDpc-w7D7lXbjcglshcn1VO2ne4neP1AF56oDNZ_VNFUAA0wdO4yrKnPNfdt2R-p76_o?purpose=inline)

`overflow: visible`

Extra content extends beyond the container. This is the default behavior and may overlap other elements.

[CSS | Overflow | overflow | Codecademy](https://images.openai.com/static-rsc-4/prlZYiXLtKP5OCzaWYncFLlXLwQzXlehXfosfUqqd2qDwJMj1EnqFqwRtbi79izOQZ9SCZRcrjOH5KCVjjA_ykekTZPYO2EBfdZDVhHWa-Lp2IqBIFainDVCDN89ZQ00PrOvQ6MBNcaZFz-fV4sMKW1nLtq-dnTKW44XJt1B6rU?purpose=inline)

`overflow: hidden`

Content beyond the container's boundaries is clipped, with no scrollbar to access the hidden portion.

[Mastering CSS Coding: Getting Started — Smashing Magazine](https://images.openai.com/static-rsc-4/hAx-BOToc9SGLlYS8iEKwRa_-9BZlzOXByyAbRUks8oqBM789t3v8TG8hlzrxxCKtY9nOxBtA_-AfVdSuCW622GZKL21Oi-iIQlJpgqcr6lMm7Ha8O3khDZWYB18sBrr5yZlSlnUdKJAexBT5qr5iMghAv2p2c7LwQ7RT0R_NnY?purpose=inline)

`overflow: auto`

Scrollbars are provided when needed. This is useful for reading panels, chat windows, and logs.

[Let’s position it with float (in CSS) | by Anupam Roy | Medium](https://images.openai.com/static-rsc-4/uTgekyNLQHZoTKtHdMPi0OFh1OQU5KW5TXH_w7ceN5fFZxHDFd2dn3t021L89KoyLtfQpaoiI5dUHg5hwSyAqOvKWj9qmFsWriRfl0tGU8Pwoud2knrVrpNwsbRL0IbSavuGLqKtxUlnrGAQRZYqrSCKNi3iKl-sxfHuU48LM08?purpose=inline)

`overflow: scroll`

Provides scrolling even when the content fits. The appearance of scrollbars depends on the browser and operating system.

## 5. How the layout problem is fixed

The problem box has a fixed width of `900px`, which can exceed the available space on a mobile screen.

Problematic CSS:

```
.layout-problem {
    width: 900px;
}
```

Fixed CSS:

```
.layout-fixed {
    width: 100%;
    max-width: 900px;
    box-sizing: border-box;
    overflow-wrap: anywhere;
}
```

The fixed version shrinks to fit its parent while remaining no wider than 900px. `overflow-wrap: anywhere` also allows long, unbroken text to wrap instead of extending beyond the box.

## 6. OVERFLOW AND LAYOUT FIXING screenshots
![alt text](<6.3 OVERFLOW 1.png>)
![alt text](<6.3 OVERFLOW2.png>)
![alt text](<6.3 OVERFLOW3.png>)



