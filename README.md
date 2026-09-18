# Secure NFC Reader

I'm attempting to build a secure NFC reader that is sturdy and can't be easily hacked with simple tooling.

```
┌──────────────────────────┐
│  ┌────────────────────┐  │
│  │      PN532 NFC     │  │
│  └─────────┬──────────┘  │
│            │             │
│  ┌─────────┴──────────┐  │
│  │ SC16IS750 UART-SPI │  │
│  └─────────┬──────────┘  │
│            │             │
│  ┌─────────┴──────────┐  │
│  │ MAX485 RS485-UART  │  │
│  └─────────┬──────────┘  │
└────────────┼─────────────┘
             │              
           RS485
```

I ordered some parts:

| Name | Description | Price |
| ---- | ---- | ---- |
| PN532 | Small red NFC reader with SPI interface | 3.27 CHF |
| SC16IS750 | SPI to UART interface, converts SPI to a simple serial connection | 3.13 CHF |
| MAX485 | UART to RS485, exposes serial connection to the outside world | 0.76 CHF |
| Project case | A simple device box for prototyping | 3.34 CHF |
| 200g potting glue | For weather and tamper proofing | 19.76 CHF |

The plan is to support modern nfc chips, hopefully DESfire EV3.

Worst case is that i understand why commercial grade equipement costs way more than simple Wiegand style readers.
