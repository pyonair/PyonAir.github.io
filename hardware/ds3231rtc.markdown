# Real Time Clock

The DS1307 RTC module contains a clock chip with backup power from a cell battery. This means it is able to keep track of time even when the primary power supply cuts out.

You may not wish to include an RTC if you are using a GPS receiver module, as the LoPy4 will be able to retrieve current time from that.


[ds1307 Datasheet (PDF) ](/assets/documents/ds1307.pdf)

| Interface | Supply voltage |
| :--- | :--- |
| I2C | 5 V |

![](/assets/grove-rtc.jpg)

__Make sure you buy an RTC module that includes the oscillator crystal and battery mount. The clock won't run without these.__

__You might need to buy the battery separately, depending on your supplier. For the RTC shown, this is a CR1225 but some RTCs use a CR2032.__

## Current suppliers

### Grove

| Company | Price |
| :--- | :--- |
| [Seeed Studio](https://www.seeedstudio.com/Grove-RTC.html) | $6.90 |

### Non-Grove

| Company | Price |
| :--- | :--- |
| [SODIAL](https://www.amazon.co.uk/SODIAL-DS3231-AT24C32-Precision-Arduino/dp/B00K67X496/ref=sr_1_3?keywords=Real+Time+Clock+Module&qid=1560415649&s=gateway&sr=8-3) | £2.32 |
| [Ali Express](https://www.aliexpress.com/item/DS3231-AT24C32-IIC-High-Precision-RTC-Module-Clock-Timer-Memory-Module/2037934408.html?spm=2114.search0104.3.1.75a77117k07iaD&ws_ab_test=searchweb0_0,searchweb201602_9_10065_10130_10068_10547_319_317_10548_10696_10192_10190_453_10084_454_10083_10618_10307_10820_10301_10821_10303_537_536_10059_10884_10887_321_322_10103,searchweb201603_52,ppcSwitch_0&algo_expid=c43bddde-e15d-423a-9e49-d149fa24d6fc-0&algo_pvid=c43bddde-e15d-423a-9e49-d149fa24d6fc) | $1.01 |
| [Electrodragon](https://www.electrodragon.com/product/ds3231-rtc-breakout-board-r2/) | $1.80 |
|  |  |
