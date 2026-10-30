# 2.8 デバイスドライバ例(p.230)

<!-- 出典画像: images/IMG_6169.JPEG -->

以下に,ブロックデバイスドライバおよびキャラクタデバイスドライバのプログラム例を掲載します.

## 2.8.1 ブロックデバイスドライバ

```asm
;********************** A BLOCK DEVICE *********************

        TITLE   5 1/4" DISK DRIVER FOR SCP DISK-MASTER

;This driver is intended to drive up to four 5 1/4" drives
;hooked to the Seattle Computer Products DISK MASTER disk
;controller. All standard IBM PC formats are supported.

FALSE   EQU     0
TRUE    EQU     NOT FALSE

;The I/O port address of the DISK MASTER
DISK    EQU     0E0H
;DISK+0
;       1793    Command/Status
;DISK+1
;       1793    Track
;DISK+2
;       1793    Sector
;DISK+3
;       1793    Data
;DISK+4
;       Aux Command/Status
;DISK+5
;       Wait Sync

;Back side select bit
BACKBIT EQU     04H
;5 1/4" select bit
SMALBIT EQU     10H
;Double Density bit
DDBIT   EQU     08H

;Done bit in status register
DONEBIT EQU     01H

; Use table below to select head step speed.
;Step times for 5" drives
; are double that shown in the table.
;
; Step value    1771    1793
;
;       0       6ms     3ms
;       1       6ms     6ms
;       2       10ms    10ms
;       3       20ms    15ms
;
STPSPD  EQU     1

NUMERR  EQU     ERROUT-ERRIN

CR      EQU     0DH
LF      EQU     0AH
```
