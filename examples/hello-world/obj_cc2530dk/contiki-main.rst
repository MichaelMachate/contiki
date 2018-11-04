                                      1 ;--------------------------------------------------------
                                      2 ; File Created by SDCC : free open source ANSI-C Compiler
                                      3 ; Version 3.3.1 #8804 (Aug  6 2013) (Linux)
                                      4 ; This file was generated Sat Nov  3 15:45:34 2018
                                      5 ;--------------------------------------------------------
                                      6 	.module contiki_main
                                      7 	.optsdcc -mmcs51 --model-huge
                                      8 	
                                      9 ;--------------------------------------------------------
                                     10 ; Public variables in this module
                                     11 ;--------------------------------------------------------
                                     12 	.globl _main
                                     13 	.globl _random_init
                                     14 	.globl _puthex
                                     15 	.globl _putstring
                                     16 	.globl _netstack_init
                                     17 	.globl _queuebuf_init
                                     18 	.globl _packetbuf_set_datalen
                                     19 	.globl _packetbuf_dataptr
                                     20 	.globl _packetbuf_clear
                                     21 	.globl _watchdog_periodic
                                     22 	.globl _watchdog_start
                                     23 	.globl _watchdog_init
                                     24 	.globl _uart0_set_input
                                     25 	.globl _uart0_init
                                     26 	.globl _leds_off
                                     27 	.globl _leds_on
                                     28 	.globl _leds_init
                                     29 	.globl _serial_line_init
                                     30 	.globl _serial_line_input_byte
                                     31 	.globl _soc_init
                                     32 	.globl _energest_init
                                     33 	.globl _rtimer_init
                                     34 	.globl _ctimer_init
                                     35 	.globl _etimer_next_expiration_time
                                     36 	.globl _etimer_pending
                                     37 	.globl _etimer_request_poll
                                     38 	.globl _clock_time
                                     39 	.globl _clock_init
                                     40 	.globl _autostart_start
                                     41 	.globl _process_run
                                     42 	.globl _process_init
                                     43 	.globl _process_start
                                     44 	.globl _memcpy
                                     45 	.globl _ACTIVE
                                     46 	.globl _TX_BYTE
                                     47 	.globl _RX_BYTE
                                     48 	.globl _ERR
                                     49 	.globl _FE
                                     50 	.globl _SLAVE
                                     51 	.globl _RE
                                     52 	.globl _MODE
                                     53 	.globl _T3OVFIF
                                     54 	.globl _T3CH0IF
                                     55 	.globl _T3CH1IF
                                     56 	.globl _T4OVFIF
                                     57 	.globl _T4CH0IF
                                     58 	.globl _T4CH1IF
                                     59 	.globl _OVFIM
                                     60 	.globl _B_0
                                     61 	.globl _B_1
                                     62 	.globl _B_2
                                     63 	.globl _B_3
                                     64 	.globl _B_4
                                     65 	.globl _B_5
                                     66 	.globl _B_6
                                     67 	.globl _B_7
                                     68 	.globl _P2IF
                                     69 	.globl _UTX0IF
                                     70 	.globl _UTX1IF
                                     71 	.globl _P1IF
                                     72 	.globl _WDTIF
                                     73 	.globl _ACC_0
                                     74 	.globl _ACC_1
                                     75 	.globl _ACC_2
                                     76 	.globl _ACC_3
                                     77 	.globl _ACC_4
                                     78 	.globl _ACC_5
                                     79 	.globl _ACC_6
                                     80 	.globl _ACC_7
                                     81 	.globl _P
                                     82 	.globl _F1
                                     83 	.globl _OV
                                     84 	.globl _RS0
                                     85 	.globl _RS1
                                     86 	.globl _F0
                                     87 	.globl _AC
                                     88 	.globl _CY
                                     89 	.globl _DMAIF
                                     90 	.globl _T1IF
                                     91 	.globl _T2IF
                                     92 	.globl _T3IF
                                     93 	.globl _T4IF
                                     94 	.globl _P0IF
                                     95 	.globl _STIF
                                     96 	.globl _DMAIE
                                     97 	.globl _T1IE
                                     98 	.globl _T2IE
                                     99 	.globl _T3IE
                                    100 	.globl _T4IE
                                    101 	.globl _P0IE
                                    102 	.globl _RFERRIE
                                    103 	.globl _ADCIE
                                    104 	.globl _URX0IE
                                    105 	.globl _URX1IE
                                    106 	.globl _ENCIE
                                    107 	.globl _STIE
                                    108 	.globl _EA
                                    109 	.globl _P2_0
                                    110 	.globl _P2_1
                                    111 	.globl _P2_2
                                    112 	.globl _P2_3
                                    113 	.globl _P2_4
                                    114 	.globl _P2_5
                                    115 	.globl _P2_6
                                    116 	.globl _P2_7
                                    117 	.globl _ENCIF_0
                                    118 	.globl _ENCIF_1
                                    119 	.globl _P1_0
                                    120 	.globl _P1_1
                                    121 	.globl _P1_2
                                    122 	.globl _P1_3
                                    123 	.globl _P1_4
                                    124 	.globl _P1_5
                                    125 	.globl _P1_6
                                    126 	.globl _P1_7
                                    127 	.globl _IT0
                                    128 	.globl _RFERRIF
                                    129 	.globl _IT1
                                    130 	.globl _URX0IF
                                    131 	.globl _ADCIF
                                    132 	.globl _URX1IF
                                    133 	.globl _P0_0
                                    134 	.globl _P0_1
                                    135 	.globl _P0_2
                                    136 	.globl _P0_3
                                    137 	.globl _P0_4
                                    138 	.globl _P0_5
                                    139 	.globl _P0_6
                                    140 	.globl _P0_7
                                    141 	.globl _WDCTL
                                    142 	.globl _U1GCR
                                    143 	.globl _U1UCR
                                    144 	.globl _U1BAUD
                                    145 	.globl _U1DBUF
                                    146 	.globl _U1CSR
                                    147 	.globl _U0GCR
                                    148 	.globl _U0UCR
                                    149 	.globl _U0BAUD
                                    150 	.globl _U0DBUF
                                    151 	.globl _U0CSR
                                    152 	.globl _TIMIF
                                    153 	.globl _T4CC1
                                    154 	.globl _T4CCTL1
                                    155 	.globl _T4CC0
                                    156 	.globl _T4CCTL0
                                    157 	.globl _T4CTL
                                    158 	.globl _T4CNT
                                    159 	.globl _T3CC1
                                    160 	.globl _T3CCTL1
                                    161 	.globl _T3CC0
                                    162 	.globl _T3CCTL0
                                    163 	.globl _T3CTL
                                    164 	.globl _T3CNT
                                    165 	.globl _T2MSEL
                                    166 	.globl _T2IRQM
                                    167 	.globl _T2MOVF2
                                    168 	.globl _T2MOVF1
                                    169 	.globl _T2MOVF0
                                    170 	.globl _T2M1
                                    171 	.globl _T2M0
                                    172 	.globl _T2IRQF
                                    173 	.globl _T2EVTCFG
                                    174 	.globl _T2CTRL
                                    175 	.globl _T1STAT
                                    176 	.globl _T1CCTL2
                                    177 	.globl _T1CCTL1
                                    178 	.globl _T1CCTL0
                                    179 	.globl _T1CTL
                                    180 	.globl _T1CNTH
                                    181 	.globl _T1CNTL
                                    182 	.globl _T1CC2H
                                    183 	.globl _T1CC2L
                                    184 	.globl _T1CC1H
                                    185 	.globl _T1CC1L
                                    186 	.globl _T1CC0H
                                    187 	.globl _T1CC0L
                                    188 	.globl _CLKCONSTA
                                    189 	.globl _CLKCONCMD
                                    190 	.globl _SLEEPSTA
                                    191 	.globl _SLEEPCMD
                                    192 	.globl _STLOAD
                                    193 	.globl _ST2
                                    194 	.globl _ST1
                                    195 	.globl _ST0
                                    196 	.globl _RFERRF
                                    197 	.globl _RFIRQF0
                                    198 	.globl _RFST
                                    199 	.globl _RFD
                                    200 	.globl _RFIRQF1
                                    201 	.globl _PSBANK
                                    202 	.globl _FMAP
                                    203 	.globl _MEMCTR
                                    204 	.globl __XPAGE
                                    205 	.globl _MPAGE
                                    206 	.globl _PMUX
                                    207 	.globl _P2DIR
                                    208 	.globl _P1DIR
                                    209 	.globl _P0DIR
                                    210 	.globl _P2INP
                                    211 	.globl _P1INP
                                    212 	.globl _P2SEL
                                    213 	.globl _P1SEL
                                    214 	.globl _P0SEL
                                    215 	.globl _APCFG
                                    216 	.globl _PERCFG
                                    217 	.globl _P0INP
                                    218 	.globl _P2IEN
                                    219 	.globl _P1IEN
                                    220 	.globl _P0IEN
                                    221 	.globl _PICTL
                                    222 	.globl _P2IFG
                                    223 	.globl _P1IFG
                                    224 	.globl _P0IFG
                                    225 	.globl _DMAREQ
                                    226 	.globl _DMAARM
                                    227 	.globl _DMA0CFGH
                                    228 	.globl _DMA0CFGL
                                    229 	.globl _DMA1CFGH
                                    230 	.globl _DMA1CFGL
                                    231 	.globl _DMAIRQ
                                    232 	.globl _ENCCS
                                    233 	.globl _ENCDO
                                    234 	.globl _ENCDI
                                    235 	.globl _RNDH
                                    236 	.globl _RNDL
                                    237 	.globl _ADCH
                                    238 	.globl _ADCL
                                    239 	.globl _ADCCON3
                                    240 	.globl _ADCCON2
                                    241 	.globl _ADCCON1
                                    242 	.globl _B
                                    243 	.globl _IRCON2
                                    244 	.globl _ACC
                                    245 	.globl _PSW
                                    246 	.globl _IRCON
                                    247 	.globl _IP1
                                    248 	.globl _IEN1
                                    249 	.globl _IP0
                                    250 	.globl _IEN0
                                    251 	.globl _P2
                                    252 	.globl _S1CON
                                    253 	.globl _IEN2
                                    254 	.globl _S0CON
                                    255 	.globl _DPS
                                    256 	.globl _P1
                                    257 	.globl _TCON
                                    258 	.globl _PCON
                                    259 	.globl _DPH1
                                    260 	.globl _DPL1
                                    261 	.globl _DPH0
                                    262 	.globl _DPL0
                                    263 	.globl _SP
                                    264 	.globl _P0
                                    265 	.globl _X_IEEE_ADDR
                                    266 	.globl _X_INFOPAGE
                                    267 	.globl _X_P2DIR
                                    268 	.globl _X_P1DIR
                                    269 	.globl _X_P0DIR
                                    270 	.globl _X_U1GCR
                                    271 	.globl _X_U1UCR
                                    272 	.globl _X_U1BAUD
                                    273 	.globl _X_U1DBUF
                                    274 	.globl _X_U1CSR
                                    275 	.globl _X_P2INP
                                    276 	.globl _X_P1INP
                                    277 	.globl _X_P2SEL
                                    278 	.globl _X_P1SEL
                                    279 	.globl _X_P0SEL
                                    280 	.globl _X_APCFG
                                    281 	.globl _X_PERCFG
                                    282 	.globl _X_T4CC1
                                    283 	.globl _X_T4CCTL1
                                    284 	.globl _X_T4CC0
                                    285 	.globl _X_T4CCTL0
                                    286 	.globl _X_T4CTL
                                    287 	.globl _X_T4CNT
                                    288 	.globl _X_RFIRQF0
                                    289 	.globl _X_T1CCTL2
                                    290 	.globl _X_T1CCTL1
                                    291 	.globl _X_T1CCTL0
                                    292 	.globl _X_T1CTL
                                    293 	.globl _X_T1CNTH
                                    294 	.globl _X_T1CNTL
                                    295 	.globl _X_RFST
                                    296 	.globl _X_T1CC2H
                                    297 	.globl _X_T1CC2L
                                    298 	.globl _X_T1CC1H
                                    299 	.globl _X_T1CC1L
                                    300 	.globl _X_T1CC0H
                                    301 	.globl _X_T1CC0L
                                    302 	.globl _X_RFD
                                    303 	.globl _X_TIMIF
                                    304 	.globl _X_DMAREQ
                                    305 	.globl _X_DMAARM
                                    306 	.globl _X_DMA0CFGH
                                    307 	.globl _X_DMA0CFGL
                                    308 	.globl _X_DMA1CFGH
                                    309 	.globl _X_DMA1CFGL
                                    310 	.globl _X_DMAIRQ
                                    311 	.globl _X_T3CC1
                                    312 	.globl _X_T3CCTL1
                                    313 	.globl _X_T3CC0
                                    314 	.globl _X_T3CCTL0
                                    315 	.globl _X_T3CTL
                                    316 	.globl _X_T3CNT
                                    317 	.globl _X_WDCTL
                                    318 	.globl _X_MEMCTR
                                    319 	.globl _X_CLKCONCMD
                                    320 	.globl _X_U0GCR
                                    321 	.globl _X_U0UCR
                                    322 	.globl _X_T2MSEL
                                    323 	.globl _X_U0BAUD
                                    324 	.globl _X_U0DBUF
                                    325 	.globl _X_RFERRF
                                    326 	.globl _X_SLEEPCMD
                                    327 	.globl _X_RNDH
                                    328 	.globl _X_RNDL
                                    329 	.globl _X_ADCH
                                    330 	.globl _X_ADCL
                                    331 	.globl _X_ADCCON3
                                    332 	.globl _X_ADCCON2
                                    333 	.globl _X_ADCCON1
                                    334 	.globl _X_ENCCS
                                    335 	.globl _X_ENCDO
                                    336 	.globl _X_ENCDI
                                    337 	.globl _X_T1STAT
                                    338 	.globl _X_PMUX
                                    339 	.globl _X_STLOAD
                                    340 	.globl _X_P2IEN
                                    341 	.globl _X_P0IEN
                                    342 	.globl _X_T2IRQM
                                    343 	.globl _X_T2MOVF2
                                    344 	.globl _X_T2MOVF1
                                    345 	.globl _X_T2MOVF0
                                    346 	.globl _X_T2M1
                                    347 	.globl _X_T2M0
                                    348 	.globl _X_T2IRQF
                                    349 	.globl _X_P2
                                    350 	.globl _X_PSBANK
                                    351 	.globl _X_FMAP
                                    352 	.globl _X_CLKCONSTA
                                    353 	.globl _X_SLEEPSTA
                                    354 	.globl _X_T2EVTCFG
                                    355 	.globl _X_ST2
                                    356 	.globl _X_ST1
                                    357 	.globl _X_ST0
                                    358 	.globl _X_T2CTRL
                                    359 	.globl _X__XPAGE
                                    360 	.globl _X_MPAGE
                                    361 	.globl _X_RFIRQF1
                                    362 	.globl _X_P1
                                    363 	.globl _X_P0INP
                                    364 	.globl _X_P1IEN
                                    365 	.globl _X_PICTL
                                    366 	.globl _X_P2IFG
                                    367 	.globl _X_P1IFG
                                    368 	.globl _X_P0IFG
                                    369 	.globl _X_U0CSR
                                    370 	.globl _X_P0
                                    371 	.globl _USBF5
                                    372 	.globl _USBF4
                                    373 	.globl _USBF3
                                    374 	.globl _USBF2
                                    375 	.globl _USBF1
                                    376 	.globl _USBF0
                                    377 	.globl _USBCNTH
                                    378 	.globl _USBCNTL
                                    379 	.globl _USBCNT0
                                    380 	.globl _USBCSOH
                                    381 	.globl _USBCSOL
                                    382 	.globl _USBMAXO
                                    383 	.globl _USBCSIH
                                    384 	.globl _USBCSIL
                                    385 	.globl _USBCS0
                                    386 	.globl _USBMAXI
                                    387 	.globl _USBCTRL
                                    388 	.globl _USBINDEX
                                    389 	.globl _USBFRMH
                                    390 	.globl _USBFRML
                                    391 	.globl _USBCIE
                                    392 	.globl _USBOIE
                                    393 	.globl _USBIIE
                                    394 	.globl _USBCIF
                                    395 	.globl _USBOIF
                                    396 	.globl _USBIIF
                                    397 	.globl _USBPOW
                                    398 	.globl _USBADDR
                                    399 	.globl _CSPT
                                    400 	.globl _CSPZ
                                    401 	.globl _CSPY
                                    402 	.globl _CSPX
                                    403 	.globl _CSPSTAT
                                    404 	.globl _CSPCTRL
                                    405 	.globl _CSPPROG23
                                    406 	.globl _CSPPROG22
                                    407 	.globl _CSPPROG21
                                    408 	.globl _CSPPROG20
                                    409 	.globl _CSPPROG19
                                    410 	.globl _CSPPROG18
                                    411 	.globl _CSPPROG17
                                    412 	.globl _CSPPROG16
                                    413 	.globl _CSPPROG15
                                    414 	.globl _CSPPROG14
                                    415 	.globl _CSPPROG13
                                    416 	.globl _CSPPROG12
                                    417 	.globl _CSPPROG11
                                    418 	.globl _CSPPROG10
                                    419 	.globl _CSPPROG9
                                    420 	.globl _CSPPROG8
                                    421 	.globl _CSPPROG7
                                    422 	.globl _CSPPROG6
                                    423 	.globl _CSPPROG5
                                    424 	.globl _CSPPROG4
                                    425 	.globl _CSPPROG3
                                    426 	.globl _CSPPROG2
                                    427 	.globl _CSPPROG1
                                    428 	.globl _CSPPROG0
                                    429 	.globl _RFC_OBS_CTRL2
                                    430 	.globl _RFC_OBS_CTRL1
                                    431 	.globl _RFC_OBS_CTRL0
                                    432 	.globl _TXFILTCFG
                                    433 	.globl _PTEST1
                                    434 	.globl _PTEST0
                                    435 	.globl _ATEST
                                    436 	.globl _DACTEST2
                                    437 	.globl _DACTEST1
                                    438 	.globl _DACTEST0
                                    439 	.globl _MDMTEST1
                                    440 	.globl _MDMTEST0
                                    441 	.globl _ADCTEST2
                                    442 	.globl _ADCTEST1
                                    443 	.globl _ADCTEST0
                                    444 	.globl _AGCCTRL3
                                    445 	.globl _AGCCTRL2
                                    446 	.globl _AGCCTRL1
                                    447 	.globl _AGCCTRL0
                                    448 	.globl _FSCAL3
                                    449 	.globl _FSCAL2
                                    450 	.globl _FSCAL1
                                    451 	.globl _FSCAL0
                                    452 	.globl _FSCTRL
                                    453 	.globl _RXCTRL
                                    454 	.globl _FREQEST
                                    455 	.globl _MDMCTRL1
                                    456 	.globl _MDMCTRL0
                                    457 	.globl _RFRND
                                    458 	.globl _RFERRM
                                    459 	.globl _RFIRQM1
                                    460 	.globl _RFIRQM0
                                    461 	.globl _TXLAST_PTR
                                    462 	.globl _TXFIRST_PTR
                                    463 	.globl _RXP1_PTR
                                    464 	.globl _RXLAST_PTR
                                    465 	.globl _RXFIRST_PTR
                                    466 	.globl _TXFIFOCNT
                                    467 	.globl _RXFIFOCNT
                                    468 	.globl _RXFIRST
                                    469 	.globl _RSSISTAT
                                    470 	.globl _RSSI
                                    471 	.globl _CCACTRL1
                                    472 	.globl _CCACTRL0
                                    473 	.globl _FSMCTRL
                                    474 	.globl _FIFOPCTRL
                                    475 	.globl _FSMSTAT1
                                    476 	.globl _FSMSTAT0
                                    477 	.globl _TXCTRL
                                    478 	.globl _TXPOWER
                                    479 	.globl _FREQCTRL
                                    480 	.globl _FREQTUNE
                                    481 	.globl _RXMASKCLR
                                    482 	.globl _RXMASKSET
                                    483 	.globl _RXENABLE
                                    484 	.globl _FRMCTRL1
                                    485 	.globl _FRMCTRL0
                                    486 	.globl _SRCEXTEN2
                                    487 	.globl _SRCEXTEN1
                                    488 	.globl _SRCEXTEN0
                                    489 	.globl _SRCSHORTEN2
                                    490 	.globl _SRCSHORTEN1
                                    491 	.globl _SRCSHORTEN0
                                    492 	.globl _SRCMATCH
                                    493 	.globl _FRMFILT1
                                    494 	.globl _FRMFILT0
                                    495 	.globl _SHORT_ADDR1
                                    496 	.globl _SHORT_ADDR0
                                    497 	.globl _PAN_ID1
                                    498 	.globl _PAN_ID0
                                    499 	.globl _EXT_ADDR7
                                    500 	.globl _EXT_ADDR6
                                    501 	.globl _EXT_ADDR5
                                    502 	.globl _EXT_ADDR4
                                    503 	.globl _EXT_ADDR3
                                    504 	.globl _EXT_ADDR2
                                    505 	.globl _EXT_ADDR1
                                    506 	.globl _EXT_ADDR0
                                    507 	.globl _SRCSHORTPENDEN2
                                    508 	.globl _SRCSHORTPENDEN1
                                    509 	.globl _SRCSHORTPENDEN0
                                    510 	.globl _SRCEXTPENDEN2
                                    511 	.globl _SRCEXTPENDEN1
                                    512 	.globl _SRCEXTPENDEN0
                                    513 	.globl _SRCRESINDEX
                                    514 	.globl _SRCRESMASK2
                                    515 	.globl _SRCRESMASK1
                                    516 	.globl _SRCRESMASK0
                                    517 	.globl _SRC_ADDR_TABLE
                                    518 	.globl _TXFIFO
                                    519 	.globl _RXFIFO
                                    520 	.globl _RFCORE_RAM
                                    521 	.globl _CMPCTL
                                    522 	.globl _OPAMPS
                                    523 	.globl _OPAMPC
                                    524 	.globl _STCV2
                                    525 	.globl _STCV1
                                    526 	.globl _STCV0
                                    527 	.globl _STCS
                                    528 	.globl _STCC
                                    529 	.globl _T1CC4H
                                    530 	.globl _T1CC4L
                                    531 	.globl _T1CC3H
                                    532 	.globl _T1CC3L
                                    533 	.globl _XX_T1CC2H
                                    534 	.globl _XX_T1CC2L
                                    535 	.globl _XX_T1CC1H
                                    536 	.globl _XX_T1CC1L
                                    537 	.globl _XX_T1CC0H
                                    538 	.globl _XX_T1CC0L
                                    539 	.globl _T1CCTL4
                                    540 	.globl _T1CCTL3
                                    541 	.globl _XX_T1CCTL2
                                    542 	.globl _XX_T1CCTL1
                                    543 	.globl _XX_T1CCTL0
                                    544 	.globl _CLD
                                    545 	.globl _IRCTL
                                    546 	.globl _CHIPINFO1
                                    547 	.globl _CHIPINFO0
                                    548 	.globl _FWDATA
                                    549 	.globl _FADDRH
                                    550 	.globl _FADDRL
                                    551 	.globl _FCTL
                                    552 	.globl _IVCTRL
                                    553 	.globl _BATTMON
                                    554 	.globl _SRCRC
                                    555 	.globl _DBGDATA
                                    556 	.globl _TESTREG0
                                    557 	.globl _CHIPID
                                    558 	.globl _CHVER
                                    559 	.globl _OBSSEL5
                                    560 	.globl _OBSSEL4
                                    561 	.globl _OBSSEL3
                                    562 	.globl _OBSSEL2
                                    563 	.globl _OBSSEL1
                                    564 	.globl _OBSSEL0
                                    565 	.globl _I2CIO
                                    566 	.globl _I2CWC
                                    567 	.globl _I2CADDR
                                    568 	.globl _I2CDATA
                                    569 	.globl _I2CSTAT
                                    570 	.globl _I2CCFG
                                    571 	.globl _OPAMPMC
                                    572 	.globl _MONMUX
                                    573 ;--------------------------------------------------------
                                    574 ; special function registers
                                    575 ;--------------------------------------------------------
                                    576 	.area RSEG    (ABS,DATA)
      000000                        577 	.org 0x0000
                           000080   578 _P0	=	0x0080
                           000081   579 _SP	=	0x0081
                           000082   580 _DPL0	=	0x0082
                           000083   581 _DPH0	=	0x0083
                           000084   582 _DPL1	=	0x0084
                           000085   583 _DPH1	=	0x0085
                           000087   584 _PCON	=	0x0087
                           000088   585 _TCON	=	0x0088
                           000090   586 _P1	=	0x0090
                           000092   587 _DPS	=	0x0092
                           000098   588 _S0CON	=	0x0098
                           00009A   589 _IEN2	=	0x009a
                           00009B   590 _S1CON	=	0x009b
                           0000A0   591 _P2	=	0x00a0
                           0000A8   592 _IEN0	=	0x00a8
                           0000A9   593 _IP0	=	0x00a9
                           0000B8   594 _IEN1	=	0x00b8
                           0000B9   595 _IP1	=	0x00b9
                           0000C0   596 _IRCON	=	0x00c0
                           0000D0   597 _PSW	=	0x00d0
                           0000E0   598 _ACC	=	0x00e0
                           0000E8   599 _IRCON2	=	0x00e8
                           0000F0   600 _B	=	0x00f0
                           0000B4   601 _ADCCON1	=	0x00b4
                           0000B5   602 _ADCCON2	=	0x00b5
                           0000B6   603 _ADCCON3	=	0x00b6
                           0000BA   604 _ADCL	=	0x00ba
                           0000BB   605 _ADCH	=	0x00bb
                           0000BC   606 _RNDL	=	0x00bc
                           0000BD   607 _RNDH	=	0x00bd
                           0000B1   608 _ENCDI	=	0x00b1
                           0000B2   609 _ENCDO	=	0x00b2
                           0000B3   610 _ENCCS	=	0x00b3
                           0000D1   611 _DMAIRQ	=	0x00d1
                           0000D2   612 _DMA1CFGL	=	0x00d2
                           0000D3   613 _DMA1CFGH	=	0x00d3
                           0000D4   614 _DMA0CFGL	=	0x00d4
                           0000D5   615 _DMA0CFGH	=	0x00d5
                           0000D6   616 _DMAARM	=	0x00d6
                           0000D7   617 _DMAREQ	=	0x00d7
                           000089   618 _P0IFG	=	0x0089
                           00008A   619 _P1IFG	=	0x008a
                           00008B   620 _P2IFG	=	0x008b
                           00008C   621 _PICTL	=	0x008c
                           0000AB   622 _P0IEN	=	0x00ab
                           00008D   623 _P1IEN	=	0x008d
                           0000AC   624 _P2IEN	=	0x00ac
                           00008F   625 _P0INP	=	0x008f
                           0000F1   626 _PERCFG	=	0x00f1
                           0000F2   627 _APCFG	=	0x00f2
                           0000F3   628 _P0SEL	=	0x00f3
                           0000F4   629 _P1SEL	=	0x00f4
                           0000F5   630 _P2SEL	=	0x00f5
                           0000F6   631 _P1INP	=	0x00f6
                           0000F7   632 _P2INP	=	0x00f7
                           0000FD   633 _P0DIR	=	0x00fd
                           0000FE   634 _P1DIR	=	0x00fe
                           0000FF   635 _P2DIR	=	0x00ff
                           0000AE   636 _PMUX	=	0x00ae
                           000093   637 _MPAGE	=	0x0093
                           000093   638 __XPAGE	=	0x0093
                           0000C7   639 _MEMCTR	=	0x00c7
                           00009F   640 _FMAP	=	0x009f
                           00009F   641 _PSBANK	=	0x009f
                           000091   642 _RFIRQF1	=	0x0091
                           0000D9   643 _RFD	=	0x00d9
                           0000E1   644 _RFST	=	0x00e1
                           0000E9   645 _RFIRQF0	=	0x00e9
                           0000BF   646 _RFERRF	=	0x00bf
                           000095   647 _ST0	=	0x0095
                           000096   648 _ST1	=	0x0096
                           000097   649 _ST2	=	0x0097
                           0000AD   650 _STLOAD	=	0x00ad
                           0000BE   651 _SLEEPCMD	=	0x00be
                           00009D   652 _SLEEPSTA	=	0x009d
                           0000C6   653 _CLKCONCMD	=	0x00c6
                           00009E   654 _CLKCONSTA	=	0x009e
                           0000DA   655 _T1CC0L	=	0x00da
                           0000DB   656 _T1CC0H	=	0x00db
                           0000DC   657 _T1CC1L	=	0x00dc
                           0000DD   658 _T1CC1H	=	0x00dd
                           0000DE   659 _T1CC2L	=	0x00de
                           0000DF   660 _T1CC2H	=	0x00df
                           0000E2   661 _T1CNTL	=	0x00e2
                           0000E3   662 _T1CNTH	=	0x00e3
                           0000E4   663 _T1CTL	=	0x00e4
                           0000E5   664 _T1CCTL0	=	0x00e5
                           0000E6   665 _T1CCTL1	=	0x00e6
                           0000E7   666 _T1CCTL2	=	0x00e7
                           0000AF   667 _T1STAT	=	0x00af
                           000094   668 _T2CTRL	=	0x0094
                           00009C   669 _T2EVTCFG	=	0x009c
                           0000A1   670 _T2IRQF	=	0x00a1
                           0000A2   671 _T2M0	=	0x00a2
                           0000A3   672 _T2M1	=	0x00a3
                           0000A4   673 _T2MOVF0	=	0x00a4
                           0000A5   674 _T2MOVF1	=	0x00a5
                           0000A6   675 _T2MOVF2	=	0x00a6
                           0000A7   676 _T2IRQM	=	0x00a7
                           0000C3   677 _T2MSEL	=	0x00c3
                           0000CA   678 _T3CNT	=	0x00ca
                           0000CB   679 _T3CTL	=	0x00cb
                           0000CC   680 _T3CCTL0	=	0x00cc
                           0000CD   681 _T3CC0	=	0x00cd
                           0000CE   682 _T3CCTL1	=	0x00ce
                           0000CF   683 _T3CC1	=	0x00cf
                           0000EA   684 _T4CNT	=	0x00ea
                           0000EB   685 _T4CTL	=	0x00eb
                           0000EC   686 _T4CCTL0	=	0x00ec
                           0000ED   687 _T4CC0	=	0x00ed
                           0000EE   688 _T4CCTL1	=	0x00ee
                           0000EF   689 _T4CC1	=	0x00ef
                           0000D8   690 _TIMIF	=	0x00d8
                           000086   691 _U0CSR	=	0x0086
                           0000C1   692 _U0DBUF	=	0x00c1
                           0000C2   693 _U0BAUD	=	0x00c2
                           0000C4   694 _U0UCR	=	0x00c4
                           0000C5   695 _U0GCR	=	0x00c5
                           0000F8   696 _U1CSR	=	0x00f8
                           0000F9   697 _U1DBUF	=	0x00f9
                           0000FA   698 _U1BAUD	=	0x00fa
                           0000FB   699 _U1UCR	=	0x00fb
                           0000FC   700 _U1GCR	=	0x00fc
                           0000C9   701 _WDCTL	=	0x00c9
                                    702 ;--------------------------------------------------------
                                    703 ; special function bits
                                    704 ;--------------------------------------------------------
                                    705 	.area RSEG    (ABS,DATA)
      000000                        706 	.org 0x0000
                           000087   707 _P0_7	=	0x0087
                           000086   708 _P0_6	=	0x0086
                           000085   709 _P0_5	=	0x0085
                           000084   710 _P0_4	=	0x0084
                           000083   711 _P0_3	=	0x0083
                           000082   712 _P0_2	=	0x0082
                           000081   713 _P0_1	=	0x0081
                           000080   714 _P0_0	=	0x0080
                           00008F   715 _URX1IF	=	0x008f
                           00008D   716 _ADCIF	=	0x008d
                           00008B   717 _URX0IF	=	0x008b
                           00008A   718 _IT1	=	0x008a
                           000089   719 _RFERRIF	=	0x0089
                           000088   720 _IT0	=	0x0088
                           000097   721 _P1_7	=	0x0097
                           000096   722 _P1_6	=	0x0096
                           000095   723 _P1_5	=	0x0095
                           000094   724 _P1_4	=	0x0094
                           000093   725 _P1_3	=	0x0093
                           000092   726 _P1_2	=	0x0092
                           000091   727 _P1_1	=	0x0091
                           000090   728 _P1_0	=	0x0090
                           000099   729 _ENCIF_1	=	0x0099
                           000098   730 _ENCIF_0	=	0x0098
                           0000A7   731 _P2_7	=	0x00a7
                           0000A6   732 _P2_6	=	0x00a6
                           0000A5   733 _P2_5	=	0x00a5
                           0000A4   734 _P2_4	=	0x00a4
                           0000A3   735 _P2_3	=	0x00a3
                           0000A2   736 _P2_2	=	0x00a2
                           0000A1   737 _P2_1	=	0x00a1
                           0000A0   738 _P2_0	=	0x00a0
                           0000AF   739 _EA	=	0x00af
                           0000AD   740 _STIE	=	0x00ad
                           0000AC   741 _ENCIE	=	0x00ac
                           0000AB   742 _URX1IE	=	0x00ab
                           0000AA   743 _URX0IE	=	0x00aa
                           0000A9   744 _ADCIE	=	0x00a9
                           0000A8   745 _RFERRIE	=	0x00a8
                           0000BD   746 _P0IE	=	0x00bd
                           0000BC   747 _T4IE	=	0x00bc
                           0000BB   748 _T3IE	=	0x00bb
                           0000BA   749 _T2IE	=	0x00ba
                           0000B9   750 _T1IE	=	0x00b9
                           0000B8   751 _DMAIE	=	0x00b8
                           0000C7   752 _STIF	=	0x00c7
                           0000C5   753 _P0IF	=	0x00c5
                           0000C4   754 _T4IF	=	0x00c4
                           0000C3   755 _T3IF	=	0x00c3
                           0000C2   756 _T2IF	=	0x00c2
                           0000C1   757 _T1IF	=	0x00c1
                           0000C0   758 _DMAIF	=	0x00c0
                           0000D7   759 _CY	=	0x00d7
                           0000D6   760 _AC	=	0x00d6
                           0000D5   761 _F0	=	0x00d5
                           0000D4   762 _RS1	=	0x00d4
                           0000D3   763 _RS0	=	0x00d3
                           0000D2   764 _OV	=	0x00d2
                           0000D1   765 _F1	=	0x00d1
                           0000D0   766 _P	=	0x00d0
                           0000E7   767 _ACC_7	=	0x00e7
                           0000E6   768 _ACC_6	=	0x00e6
                           0000E5   769 _ACC_5	=	0x00e5
                           0000E4   770 _ACC_4	=	0x00e4
                           0000E3   771 _ACC_3	=	0x00e3
                           0000E2   772 _ACC_2	=	0x00e2
                           0000E1   773 _ACC_1	=	0x00e1
                           0000E0   774 _ACC_0	=	0x00e0
                           0000EC   775 _WDTIF	=	0x00ec
                           0000EB   776 _P1IF	=	0x00eb
                           0000EA   777 _UTX1IF	=	0x00ea
                           0000E9   778 _UTX0IF	=	0x00e9
                           0000E8   779 _P2IF	=	0x00e8
                           0000F7   780 _B_7	=	0x00f7
                           0000F6   781 _B_6	=	0x00f6
                           0000F5   782 _B_5	=	0x00f5
                           0000F4   783 _B_4	=	0x00f4
                           0000F3   784 _B_3	=	0x00f3
                           0000F2   785 _B_2	=	0x00f2
                           0000F1   786 _B_1	=	0x00f1
                           0000F0   787 _B_0	=	0x00f0
                           0000DE   788 _OVFIM	=	0x00de
                           0000DD   789 _T4CH1IF	=	0x00dd
                           0000DC   790 _T4CH0IF	=	0x00dc
                           0000DB   791 _T4OVFIF	=	0x00db
                           0000DA   792 _T3CH1IF	=	0x00da
                           0000D9   793 _T3CH0IF	=	0x00d9
                           0000D8   794 _T3OVFIF	=	0x00d8
                           0000FF   795 _MODE	=	0x00ff
                           0000FE   796 _RE	=	0x00fe
                           0000FD   797 _SLAVE	=	0x00fd
                           0000FC   798 _FE	=	0x00fc
                           0000FB   799 _ERR	=	0x00fb
                           0000FA   800 _RX_BYTE	=	0x00fa
                           0000F9   801 _TX_BYTE	=	0x00f9
                           0000F8   802 _ACTIVE	=	0x00f8
                                    803 ;--------------------------------------------------------
                                    804 ; overlayable register banks
                                    805 ;--------------------------------------------------------
                                    806 	.area REG_BANK_0	(REL,OVR,DATA)
      000000                        807 	.ds 8
                                    808 ;--------------------------------------------------------
                                    809 ; internal ram data
                                    810 ;--------------------------------------------------------
                                    811 	.area DSEG    (DATA)
      000008                        812 _len:
      000008                        813 	.ds 2
                                    814 ;--------------------------------------------------------
                                    815 ; overlayable items in internal ram 
                                    816 ;--------------------------------------------------------
                                    817 ;--------------------------------------------------------
                                    818 ; Stack segment in internal ram 
                                    819 ;--------------------------------------------------------
                                    820 	.area	SSEG
      000021                        821 __start__stack:
      000021                        822 	.ds	1
                                    823 
                                    824 ;--------------------------------------------------------
                                    825 ; indirectly addressable internal ram data
                                    826 ;--------------------------------------------------------
                                    827 	.area ISEG    (DATA)
                                    828 ;--------------------------------------------------------
                                    829 ; absolute internal ram data
                                    830 ;--------------------------------------------------------
                                    831 	.area IABS    (ABS,DATA)
                                    832 	.area IABS    (ABS,DATA)
                                    833 ;--------------------------------------------------------
                                    834 ; bit data
                                    835 ;--------------------------------------------------------
                                    836 	.area BSEG    (BIT)
                                    837 ;--------------------------------------------------------
                                    838 ; paged external ram data
                                    839 ;--------------------------------------------------------
                                    840 	.area PSEG    (PAG,XDATA)
                                    841 ;--------------------------------------------------------
                                    842 ; external ram data
                                    843 ;--------------------------------------------------------
                                    844 	.area XSEG    (XDATA)
                           0061A6   845 _MONMUX	=	0x61a6
                           0061A6   846 _OPAMPMC	=	0x61a6
                           006230   847 _I2CCFG	=	0x6230
                           006231   848 _I2CSTAT	=	0x6231
                           006232   849 _I2CDATA	=	0x6232
                           006233   850 _I2CADDR	=	0x6233
                           006234   851 _I2CWC	=	0x6234
                           006235   852 _I2CIO	=	0x6235
                           006243   853 _OBSSEL0	=	0x6243
                           006244   854 _OBSSEL1	=	0x6244
                           006245   855 _OBSSEL2	=	0x6245
                           006246   856 _OBSSEL3	=	0x6246
                           006247   857 _OBSSEL4	=	0x6247
                           006248   858 _OBSSEL5	=	0x6248
                           006249   859 _CHVER	=	0x6249
                           00624A   860 _CHIPID	=	0x624a
                           00624B   861 _TESTREG0	=	0x624b
                           006260   862 _DBGDATA	=	0x6260
                           006262   863 _SRCRC	=	0x6262
                           006264   864 _BATTMON	=	0x6264
                           006265   865 _IVCTRL	=	0x6265
                           006270   866 _FCTL	=	0x6270
                           006271   867 _FADDRL	=	0x6271
                           006272   868 _FADDRH	=	0x6272
                           006273   869 _FWDATA	=	0x6273
                           006276   870 _CHIPINFO0	=	0x6276
                           006277   871 _CHIPINFO1	=	0x6277
                           006281   872 _IRCTL	=	0x6281
                           006290   873 _CLD	=	0x6290
                           0062A0   874 _XX_T1CCTL0	=	0x62a0
                           0062A1   875 _XX_T1CCTL1	=	0x62a1
                           0062A2   876 _XX_T1CCTL2	=	0x62a2
                           0062A3   877 _T1CCTL3	=	0x62a3
                           0062A4   878 _T1CCTL4	=	0x62a4
                           0062A6   879 _XX_T1CC0L	=	0x62a6
                           0062A7   880 _XX_T1CC0H	=	0x62a7
                           0062A8   881 _XX_T1CC1L	=	0x62a8
                           0062A9   882 _XX_T1CC1H	=	0x62a9
                           0062AA   883 _XX_T1CC2L	=	0x62aa
                           0062AB   884 _XX_T1CC2H	=	0x62ab
                           0062AC   885 _T1CC3L	=	0x62ac
                           0062AD   886 _T1CC3H	=	0x62ad
                           0062AE   887 _T1CC4L	=	0x62ae
                           0062AF   888 _T1CC4H	=	0x62af
                           0062B0   889 _STCC	=	0x62b0
                           0062B1   890 _STCS	=	0x62b1
                           0062B2   891 _STCV0	=	0x62b2
                           0062B3   892 _STCV1	=	0x62b3
                           0062B4   893 _STCV2	=	0x62b4
                           0062C0   894 _OPAMPC	=	0x62c0
                           0062C1   895 _OPAMPS	=	0x62c1
                           0062D0   896 _CMPCTL	=	0x62d0
                           006000   897 _RFCORE_RAM	=	0x6000
                           006000   898 _RXFIFO	=	0x6000
                           006080   899 _TXFIFO	=	0x6080
                           006100   900 _SRC_ADDR_TABLE	=	0x6100
                           006160   901 _SRCRESMASK0	=	0x6160
                           006161   902 _SRCRESMASK1	=	0x6161
                           006162   903 _SRCRESMASK2	=	0x6162
                           006163   904 _SRCRESINDEX	=	0x6163
                           006164   905 _SRCEXTPENDEN0	=	0x6164
                           006165   906 _SRCEXTPENDEN1	=	0x6165
                           006166   907 _SRCEXTPENDEN2	=	0x6166
                           006167   908 _SRCSHORTPENDEN0	=	0x6167
                           006168   909 _SRCSHORTPENDEN1	=	0x6168
                           006169   910 _SRCSHORTPENDEN2	=	0x6169
                           00616A   911 _EXT_ADDR0	=	0x616a
                           00616B   912 _EXT_ADDR1	=	0x616b
                           00616C   913 _EXT_ADDR2	=	0x616c
                           00616D   914 _EXT_ADDR3	=	0x616d
                           00616E   915 _EXT_ADDR4	=	0x616e
                           00616F   916 _EXT_ADDR5	=	0x616f
                           006170   917 _EXT_ADDR6	=	0x6170
                           006171   918 _EXT_ADDR7	=	0x6171
                           006172   919 _PAN_ID0	=	0x6172
                           006173   920 _PAN_ID1	=	0x6173
                           006174   921 _SHORT_ADDR0	=	0x6174
                           006175   922 _SHORT_ADDR1	=	0x6175
                           006180   923 _FRMFILT0	=	0x6180
                           006181   924 _FRMFILT1	=	0x6181
                           006182   925 _SRCMATCH	=	0x6182
                           006183   926 _SRCSHORTEN0	=	0x6183
                           006184   927 _SRCSHORTEN1	=	0x6184
                           006185   928 _SRCSHORTEN2	=	0x6185
                           006186   929 _SRCEXTEN0	=	0x6186
                           006187   930 _SRCEXTEN1	=	0x6187
                           006188   931 _SRCEXTEN2	=	0x6188
                           006189   932 _FRMCTRL0	=	0x6189
                           00618A   933 _FRMCTRL1	=	0x618a
                           00618B   934 _RXENABLE	=	0x618b
                           00618C   935 _RXMASKSET	=	0x618c
                           00618D   936 _RXMASKCLR	=	0x618d
                           00618E   937 _FREQTUNE	=	0x618e
                           00618F   938 _FREQCTRL	=	0x618f
                           006190   939 _TXPOWER	=	0x6190
                           006191   940 _TXCTRL	=	0x6191
                           006192   941 _FSMSTAT0	=	0x6192
                           006193   942 _FSMSTAT1	=	0x6193
                           006194   943 _FIFOPCTRL	=	0x6194
                           006195   944 _FSMCTRL	=	0x6195
                           006196   945 _CCACTRL0	=	0x6196
                           006197   946 _CCACTRL1	=	0x6197
                           006198   947 _RSSI	=	0x6198
                           006199   948 _RSSISTAT	=	0x6199
                           00619A   949 _RXFIRST	=	0x619a
                           00619B   950 _RXFIFOCNT	=	0x619b
                           00619C   951 _TXFIFOCNT	=	0x619c
                           00619D   952 _RXFIRST_PTR	=	0x619d
                           00619E   953 _RXLAST_PTR	=	0x619e
                           00619F   954 _RXP1_PTR	=	0x619f
                           0061A1   955 _TXFIRST_PTR	=	0x61a1
                           0061A2   956 _TXLAST_PTR	=	0x61a2
                           0061A3   957 _RFIRQM0	=	0x61a3
                           0061A4   958 _RFIRQM1	=	0x61a4
                           0061A5   959 _RFERRM	=	0x61a5
                           0061A7   960 _RFRND	=	0x61a7
                           0061A8   961 _MDMCTRL0	=	0x61a8
                           0061A9   962 _MDMCTRL1	=	0x61a9
                           0061AA   963 _FREQEST	=	0x61aa
                           0061AB   964 _RXCTRL	=	0x61ab
                           0061AC   965 _FSCTRL	=	0x61ac
                           0061AD   966 _FSCAL0	=	0x61ad
                           0061AE   967 _FSCAL1	=	0x61ae
                           0061AF   968 _FSCAL2	=	0x61af
                           0061B0   969 _FSCAL3	=	0x61b0
                           0061B1   970 _AGCCTRL0	=	0x61b1
                           0061B2   971 _AGCCTRL1	=	0x61b2
                           0061B3   972 _AGCCTRL2	=	0x61b3
                           0061B4   973 _AGCCTRL3	=	0x61b4
                           0061B5   974 _ADCTEST0	=	0x61b5
                           0061B6   975 _ADCTEST1	=	0x61b6
                           0061B7   976 _ADCTEST2	=	0x61b7
                           0061B8   977 _MDMTEST0	=	0x61b8
                           0061B9   978 _MDMTEST1	=	0x61b9
                           0061BA   979 _DACTEST0	=	0x61ba
                           0061BB   980 _DACTEST1	=	0x61bb
                           0061BC   981 _DACTEST2	=	0x61bc
                           0061BD   982 _ATEST	=	0x61bd
                           0061BE   983 _PTEST0	=	0x61be
                           0061BF   984 _PTEST1	=	0x61bf
                           0061FA   985 _TXFILTCFG	=	0x61fa
                           0061EB   986 _RFC_OBS_CTRL0	=	0x61eb
                           0061EC   987 _RFC_OBS_CTRL1	=	0x61ec
                           0061ED   988 _RFC_OBS_CTRL2	=	0x61ed
                           0061C0   989 _CSPPROG0	=	0x61c0
                           0061C1   990 _CSPPROG1	=	0x61c1
                           0061C2   991 _CSPPROG2	=	0x61c2
                           0061C3   992 _CSPPROG3	=	0x61c3
                           0061C4   993 _CSPPROG4	=	0x61c4
                           0061C5   994 _CSPPROG5	=	0x61c5
                           0061C6   995 _CSPPROG6	=	0x61c6
                           0061C7   996 _CSPPROG7	=	0x61c7
                           0061C8   997 _CSPPROG8	=	0x61c8
                           0061C9   998 _CSPPROG9	=	0x61c9
                           0061CA   999 _CSPPROG10	=	0x61ca
                           0061CB  1000 _CSPPROG11	=	0x61cb
                           0061CC  1001 _CSPPROG12	=	0x61cc
                           0061CD  1002 _CSPPROG13	=	0x61cd
                           0061CE  1003 _CSPPROG14	=	0x61ce
                           0061CF  1004 _CSPPROG15	=	0x61cf
                           0061D0  1005 _CSPPROG16	=	0x61d0
                           0061D1  1006 _CSPPROG17	=	0x61d1
                           0061D2  1007 _CSPPROG18	=	0x61d2
                           0061D3  1008 _CSPPROG19	=	0x61d3
                           0061D4  1009 _CSPPROG20	=	0x61d4
                           0061D5  1010 _CSPPROG21	=	0x61d5
                           0061D6  1011 _CSPPROG22	=	0x61d6
                           0061D7  1012 _CSPPROG23	=	0x61d7
                           0061E0  1013 _CSPCTRL	=	0x61e0
                           0061E1  1014 _CSPSTAT	=	0x61e1
                           0061E2  1015 _CSPX	=	0x61e2
                           0061E3  1016 _CSPY	=	0x61e3
                           0061E4  1017 _CSPZ	=	0x61e4
                           0061E5  1018 _CSPT	=	0x61e5
                           006200  1019 _USBADDR	=	0x6200
                           006201  1020 _USBPOW	=	0x6201
                           006202  1021 _USBIIF	=	0x6202
                           006204  1022 _USBOIF	=	0x6204
                           006206  1023 _USBCIF	=	0x6206
                           006207  1024 _USBIIE	=	0x6207
                           006209  1025 _USBOIE	=	0x6209
                           00620B  1026 _USBCIE	=	0x620b
                           00620C  1027 _USBFRML	=	0x620c
                           00620D  1028 _USBFRMH	=	0x620d
                           00620E  1029 _USBINDEX	=	0x620e
                           00620F  1030 _USBCTRL	=	0x620f
                           006210  1031 _USBMAXI	=	0x6210
                           006211  1032 _USBCS0	=	0x6211
                           006211  1033 _USBCSIL	=	0x6211
                           006212  1034 _USBCSIH	=	0x6212
                           006213  1035 _USBMAXO	=	0x6213
                           006214  1036 _USBCSOL	=	0x6214
                           006215  1037 _USBCSOH	=	0x6215
                           006216  1038 _USBCNT0	=	0x6216
                           006216  1039 _USBCNTL	=	0x6216
                           006217  1040 _USBCNTH	=	0x6217
                           006220  1041 _USBF0	=	0x6220
                           006222  1042 _USBF1	=	0x6222
                           006224  1043 _USBF2	=	0x6224
                           006226  1044 _USBF3	=	0x6226
                           006228  1045 _USBF4	=	0x6228
                           00622A  1046 _USBF5	=	0x622a
                           007080  1047 _X_P0	=	0x7080
                           007086  1048 _X_U0CSR	=	0x7086
                           007089  1049 _X_P0IFG	=	0x7089
                           00708A  1050 _X_P1IFG	=	0x708a
                           00708B  1051 _X_P2IFG	=	0x708b
                           00708C  1052 _X_PICTL	=	0x708c
                           00708D  1053 _X_P1IEN	=	0x708d
                           00708F  1054 _X_P0INP	=	0x708f
                           007090  1055 _X_P1	=	0x7090
                           007091  1056 _X_RFIRQF1	=	0x7091
                           007093  1057 _X_MPAGE	=	0x7093
                           007093  1058 _X__XPAGE	=	0x7093
                           007094  1059 _X_T2CTRL	=	0x7094
                           007095  1060 _X_ST0	=	0x7095
                           007096  1061 _X_ST1	=	0x7096
                           007097  1062 _X_ST2	=	0x7097
                           00709C  1063 _X_T2EVTCFG	=	0x709c
                           00709D  1064 _X_SLEEPSTA	=	0x709d
                           00709E  1065 _X_CLKCONSTA	=	0x709e
                           00709F  1066 _X_FMAP	=	0x709f
                           00709F  1067 _X_PSBANK	=	0x709f
                           0070A0  1068 _X_P2	=	0x70a0
                           0070A1  1069 _X_T2IRQF	=	0x70a1
                           0070A2  1070 _X_T2M0	=	0x70a2
                           0070A3  1071 _X_T2M1	=	0x70a3
                           0070A4  1072 _X_T2MOVF0	=	0x70a4
                           0070A5  1073 _X_T2MOVF1	=	0x70a5
                           0070A6  1074 _X_T2MOVF2	=	0x70a6
                           0070A7  1075 _X_T2IRQM	=	0x70a7
                           0070AB  1076 _X_P0IEN	=	0x70ab
                           0070AC  1077 _X_P2IEN	=	0x70ac
                           0070AD  1078 _X_STLOAD	=	0x70ad
                           0070AE  1079 _X_PMUX	=	0x70ae
                           0070AF  1080 _X_T1STAT	=	0x70af
                           0070B1  1081 _X_ENCDI	=	0x70b1
                           0070B2  1082 _X_ENCDO	=	0x70b2
                           0070B3  1083 _X_ENCCS	=	0x70b3
                           0070B4  1084 _X_ADCCON1	=	0x70b4
                           0070B5  1085 _X_ADCCON2	=	0x70b5
                           0070B6  1086 _X_ADCCON3	=	0x70b6
                           0070BA  1087 _X_ADCL	=	0x70ba
                           0070BB  1088 _X_ADCH	=	0x70bb
                           0070BC  1089 _X_RNDL	=	0x70bc
                           0070BD  1090 _X_RNDH	=	0x70bd
                           0070BE  1091 _X_SLEEPCMD	=	0x70be
                           0070BF  1092 _X_RFERRF	=	0x70bf
                           0070C1  1093 _X_U0DBUF	=	0x70c1
                           0070C2  1094 _X_U0BAUD	=	0x70c2
                           0070C3  1095 _X_T2MSEL	=	0x70c3
                           0070C4  1096 _X_U0UCR	=	0x70c4
                           0070C5  1097 _X_U0GCR	=	0x70c5
                           0070C6  1098 _X_CLKCONCMD	=	0x70c6
                           0070C7  1099 _X_MEMCTR	=	0x70c7
                           0070C9  1100 _X_WDCTL	=	0x70c9
                           0070CA  1101 _X_T3CNT	=	0x70ca
                           0070CB  1102 _X_T3CTL	=	0x70cb
                           0070CC  1103 _X_T3CCTL0	=	0x70cc
                           0070CD  1104 _X_T3CC0	=	0x70cd
                           0070CE  1105 _X_T3CCTL1	=	0x70ce
                           0070CF  1106 _X_T3CC1	=	0x70cf
                           0070D1  1107 _X_DMAIRQ	=	0x70d1
                           0070D2  1108 _X_DMA1CFGL	=	0x70d2
                           0070D3  1109 _X_DMA1CFGH	=	0x70d3
                           0070D4  1110 _X_DMA0CFGL	=	0x70d4
                           0070D5  1111 _X_DMA0CFGH	=	0x70d5
                           0070D6  1112 _X_DMAARM	=	0x70d6
                           0070D7  1113 _X_DMAREQ	=	0x70d7
                           0070D8  1114 _X_TIMIF	=	0x70d8
                           0070D9  1115 _X_RFD	=	0x70d9
                           0070DA  1116 _X_T1CC0L	=	0x70da
                           0070DB  1117 _X_T1CC0H	=	0x70db
                           0070DC  1118 _X_T1CC1L	=	0x70dc
                           0070DD  1119 _X_T1CC1H	=	0x70dd
                           0070DE  1120 _X_T1CC2L	=	0x70de
                           0070DF  1121 _X_T1CC2H	=	0x70df
                           0070E1  1122 _X_RFST	=	0x70e1
                           0070E2  1123 _X_T1CNTL	=	0x70e2
                           0070E3  1124 _X_T1CNTH	=	0x70e3
                           0070E4  1125 _X_T1CTL	=	0x70e4
                           0070E5  1126 _X_T1CCTL0	=	0x70e5
                           0070E6  1127 _X_T1CCTL1	=	0x70e6
                           0070E7  1128 _X_T1CCTL2	=	0x70e7
                           0070E9  1129 _X_RFIRQF0	=	0x70e9
                           0070EA  1130 _X_T4CNT	=	0x70ea
                           0070EB  1131 _X_T4CTL	=	0x70eb
                           0070EC  1132 _X_T4CCTL0	=	0x70ec
                           0070ED  1133 _X_T4CC0	=	0x70ed
                           0070EE  1134 _X_T4CCTL1	=	0x70ee
                           0070EF  1135 _X_T4CC1	=	0x70ef
                           0070F1  1136 _X_PERCFG	=	0x70f1
                           0070F2  1137 _X_APCFG	=	0x70f2
                           0070F3  1138 _X_P0SEL	=	0x70f3
                           0070F4  1139 _X_P1SEL	=	0x70f4
                           0070F5  1140 _X_P2SEL	=	0x70f5
                           0070F6  1141 _X_P1INP	=	0x70f6
                           0070F7  1142 _X_P2INP	=	0x70f7
                           0070F8  1143 _X_U1CSR	=	0x70f8
                           0070F9  1144 _X_U1DBUF	=	0x70f9
                           0070FA  1145 _X_U1BAUD	=	0x70fa
                           0070FB  1146 _X_U1UCR	=	0x70fb
                           0070FC  1147 _X_U1GCR	=	0x70fc
                           0070FD  1148 _X_P0DIR	=	0x70fd
                           0070FE  1149 _X_P1DIR	=	0x70fe
                           0070FF  1150 _X_P2DIR	=	0x70ff
                           007800  1151 _X_INFOPAGE	=	0x7800
                           00780C  1152 _X_IEEE_ADDR	=	0x780c
                                   1153 ;--------------------------------------------------------
                                   1154 ; absolute external ram data
                                   1155 ;--------------------------------------------------------
                                   1156 	.area XABS    (ABS,XDATA)
                                   1157 ;--------------------------------------------------------
                                   1158 ; external initialized ram data
                                   1159 ;--------------------------------------------------------
                                   1160 	.area XISEG   (XDATA)
                                   1161 	.area HOME    (CODE)
                                   1162 	.area GSINIT0 (CODE)
                                   1163 	.area GSINIT1 (CODE)
                                   1164 	.area GSINIT2 (CODE)
                                   1165 	.area GSINIT3 (CODE)
                                   1166 	.area GSINIT4 (CODE)
                                   1167 	.area GSINIT5 (CODE)
                                   1168 	.area GSINIT  (CODE)
                                   1169 	.area GSFINAL (CODE)
                                   1170 	.area CSEG    (CODE)
                                   1171 ;--------------------------------------------------------
                                   1172 ; interrupt vector 
                                   1173 ;--------------------------------------------------------
                                   1174 	.area HOME    (CODE)
      000000                       1175 __interrupt_vect:
      000000 02 52 B8         [24] 1176 	ljmp	__sdcc_gsinit_startup
      000003 32               [24] 1177 	reti
      000004                       1178 	.ds	7
      00000B 32               [24] 1179 	reti
      00000C                       1180 	.ds	7
      000013 32               [24] 1181 	reti
      000014                       1182 	.ds	7
      00001B 32               [24] 1183 	reti
      00001C                       1184 	.ds	7
      000023 32               [24] 1185 	reti
      000024                       1186 	.ds	7
      00002B 02 09 81         [24] 1187 	ljmp	_clock_isr
      00002E                       1188 	.ds	5
      000033 32               [24] 1189 	reti
      000034                       1190 	.ds	7
      00003B 32               [24] 1191 	reti
      00003C                       1192 	.ds	7
      000043 32               [24] 1193 	reti
      000044                       1194 	.ds	7
      00004B 02 21 83         [24] 1195 	ljmp	_rtimer_isr
      00004E                       1196 	.ds	5
      000053 32               [24] 1197 	reti
      000054                       1198 	.ds	7
      00005B 32               [24] 1199 	reti
      00005C                       1200 	.ds	7
      000063 32               [24] 1201 	reti
      000064                       1202 	.ds	7
      00006B 02 07 72         [24] 1203 	ljmp	_port_0_isr
                                   1204 ;--------------------------------------------------------
                                   1205 ; global & static initialisations
                                   1206 ;--------------------------------------------------------
                                   1207 	.area HOME    (CODE)
                                   1208 	.area GSINIT  (CODE)
                                   1209 	.area GSFINAL (CODE)
                                   1210 	.area GSINIT  (CODE)
                                   1211 	.globl __sdcc_gsinit_startup
                                   1212 	.globl __sdcc_program_startup
                                   1213 	.globl __start__stack
                                   1214 	.globl __mcs51_genXINIT
                                   1215 	.globl __mcs51_genXRAMCLEAR
                                   1216 	.globl __mcs51_genRAMCLEAR
                                   1217 	.area GSFINAL (CODE)
      005333 02 00 6E         [24] 1218 	ljmp	__sdcc_program_startup
                                   1219 ;--------------------------------------------------------
                                   1220 ; Home
                                   1221 ;--------------------------------------------------------
                                   1222 	.area HOME    (CODE)
                                   1223 	.area HOME    (CODE)
      00006E                       1224 __sdcc_program_startup:
      00006E 02 02 DC         [24] 1225 	ljmp	_main
                                   1226 ;	return from main will return to caller
                                   1227 ;--------------------------------------------------------
                                   1228 ; code
                                   1229 ;--------------------------------------------------------
                                   1230 	.area HOME    (CODE)
                                   1231 ;------------------------------------------------------------
                                   1232 ;Allocation info for local variables in function 'fade'
                                   1233 ;------------------------------------------------------------
                                   1234 ;l                         Allocated to stack - sp -5
                                   1235 ;i                         Allocated to stack - sp -3
                                   1236 ;a                         Allocated to stack - sp -1
                                   1237 ;k                         Allocated to registers r4 r5 
                                   1238 ;j                         Allocated to registers r2 r3 
                                   1239 ;------------------------------------------------------------
                                   1240 ;	../../platform/cc2530dk/./contiki-main.c:64: fade(int l) CC_NON_BANKED
                                   1241 ;	-----------------------------------------
                                   1242 ;	 function fade
                                   1243 ;	-----------------------------------------
      000071                       1244 _fade:
                           000007  1245 	ar7 = 0x07
                           000006  1246 	ar6 = 0x06
                           000005  1247 	ar5 = 0x05
                           000004  1248 	ar4 = 0x04
                           000003  1249 	ar3 = 0x03
                           000002  1250 	ar2 = 0x02
                           000001  1251 	ar1 = 0x01
                           000000  1252 	ar0 = 0x00
      000071 C0 82            [24] 1253 	push	dpl
      000073 C0 83            [24] 1254 	push	dph
      000075 E5 81            [12] 1255 	mov	a,sp
      000077 24 04            [12] 1256 	add	a,#0x04
      000079 F5 81            [12] 1257 	mov	sp,a
                                   1258 ;	../../platform/cc2530dk/./contiki-main.c:68: for(k = 0; k < 400; ++k) {
      00007B 7C 00            [12] 1259 	mov	r4,#0x00
      00007D 7D 00            [12] 1260 	mov	r5,#0x00
      00007F                       1261 00110$:
                                   1262 ;	../../platform/cc2530dk/./contiki-main.c:69: j = k > 200 ? 400 - k : k;
      00007F C3               [12] 1263 	clr	c
      000080 74 C8            [12] 1264 	mov	a,#0xC8
      000082 9C               [12] 1265 	subb	a,r4
      000083 E4               [12] 1266 	clr	a
      000084 64 80            [12] 1267 	xrl	a,#0x80
      000086 8D F0            [24] 1268 	mov	b,r5
      000088 63 F0 80         [24] 1269 	xrl	b,#0x80
      00008B 95 F0            [12] 1270 	subb	a,b
      00008D 50 0B            [24] 1271 	jnc	00114$
      00008F 74 90            [12] 1272 	mov	a,#0x90
      000091 C3               [12] 1273 	clr	c
      000092 9C               [12] 1274 	subb	a,r4
      000093 FA               [12] 1275 	mov	r2,a
      000094 74 01            [12] 1276 	mov	a,#0x01
      000096 9D               [12] 1277 	subb	a,r5
      000097 FB               [12] 1278 	mov	r3,a
      000098 80 04            [24] 1279 	sjmp	00115$
      00009A                       1280 00114$:
      00009A 8C 02            [24] 1281 	mov	ar2,r4
      00009C 8D 03            [24] 1282 	mov	ar3,r5
      00009E                       1283 00115$:
                                   1284 ;	../../platform/cc2530dk/./contiki-main.c:71: leds_on(l);
      00009E E5 81            [12] 1285 	mov	a,sp
      0000A0 24 FB            [12] 1286 	add	a,#0xfb
      0000A2 F8               [12] 1287 	mov	r0,a
      0000A3 86 07            [24] 1288 	mov	ar7,@r0
      0000A5 8F 82            [24] 1289 	mov	dpl,r7
      0000A7 C0 07            [24] 1290 	push	ar7
      0000A9 C0 05            [24] 1291 	push	ar5
      0000AB C0 04            [24] 1292 	push	ar4
      0000AD C0 03            [24] 1293 	push	ar3
      0000AF C0 02            [24] 1294 	push	ar2
      0000B1 78 0F            [12] 1295 	mov	r0,#_leds_on
      0000B3 79 81            [12] 1296 	mov	r1,#(_leds_on >> 8)
      0000B5 7A 04            [12] 1297 	mov	r2,#(_leds_on >> 16)
      0000B7 12 08 14         [24] 1298 	lcall	__sdcc_banked_call
      0000BA D0 02            [24] 1299 	pop	ar2
      0000BC D0 03            [24] 1300 	pop	ar3
      0000BE D0 04            [24] 1301 	pop	ar4
      0000C0 D0 05            [24] 1302 	pop	ar5
      0000C2 D0 07            [24] 1303 	pop	ar7
                                   1304 ;	../../platform/cc2530dk/./contiki-main.c:72: for(i = 0; i < j; ++i) {
      0000C4 E5 81            [12] 1305 	mov	a,sp
      0000C6 24 FD            [12] 1306 	add	a,#0xfd
      0000C8 F8               [12] 1307 	mov	r0,a
      0000C9 E4               [12] 1308 	clr	a
      0000CA F6               [12] 1309 	mov	@r0,a
      0000CB 08               [12] 1310 	inc	r0
      0000CC F6               [12] 1311 	mov	@r0,a
      0000CD                       1312 00105$:
      0000CD E5 81            [12] 1313 	mov	a,sp
      0000CF 24 FD            [12] 1314 	add	a,#0xfd
      0000D1 F8               [12] 1315 	mov	r0,a
      0000D2 C3               [12] 1316 	clr	c
      0000D3 E6               [12] 1317 	mov	a,@r0
      0000D4 9A               [12] 1318 	subb	a,r2
      0000D5 08               [12] 1319 	inc	r0
      0000D6 E6               [12] 1320 	mov	a,@r0
      0000D7 64 80            [12] 1321 	xrl	a,#0x80
      0000D9 8B F0            [24] 1322 	mov	b,r3
      0000DB 63 F0 80         [24] 1323 	xrl	b,#0x80
      0000DE 95 F0            [12] 1324 	subb	a,b
      0000E0 50 1D            [24] 1325 	jnc	00101$
                                   1326 ;	../../platform/cc2530dk/./contiki-main.c:73: a = i;
      0000E2 E5 81            [12] 1327 	mov	a,sp
      0000E4 24 FD            [12] 1328 	add	a,#0xfd
      0000E6 F8               [12] 1329 	mov	r0,a
      0000E7 A9 81            [24] 1330 	mov	r1,sp
      0000E9 19               [12] 1331 	dec	r1
      0000EA E6               [12] 1332 	mov	a,@r0
      0000EB F7               [12] 1333 	mov	@r1,a
      0000EC 08               [12] 1334 	inc	r0
      0000ED 09               [12] 1335 	inc	r1
      0000EE E6               [12] 1336 	mov	a,@r0
      0000EF F7               [12] 1337 	mov	@r1,a
                                   1338 ;	../../platform/cc2530dk/./contiki-main.c:72: for(i = 0; i < j; ++i) {
      0000F0 E5 81            [12] 1339 	mov	a,sp
      0000F2 24 FD            [12] 1340 	add	a,#0xfd
      0000F4 F8               [12] 1341 	mov	r0,a
      0000F5 74 01            [12] 1342 	mov	a,#0x01
      0000F7 26               [12] 1343 	add	a,@r0
      0000F8 F6               [12] 1344 	mov	@r0,a
      0000F9 E4               [12] 1345 	clr	a
      0000FA 08               [12] 1346 	inc	r0
      0000FB 36               [12] 1347 	addc	a,@r0
      0000FC F6               [12] 1348 	mov	@r0,a
      0000FD 80 CE            [24] 1349 	sjmp	00105$
      0000FF                       1350 00101$:
                                   1351 ;	../../platform/cc2530dk/./contiki-main.c:75: leds_off(l);
      0000FF 8F 82            [24] 1352 	mov	dpl,r7
      000101 C0 05            [24] 1353 	push	ar5
      000103 C0 04            [24] 1354 	push	ar4
      000105 C0 03            [24] 1355 	push	ar3
      000107 C0 02            [24] 1356 	push	ar2
      000109 78 25            [12] 1357 	mov	r0,#_leds_off
      00010B 79 81            [12] 1358 	mov	r1,#(_leds_off >> 8)
      00010D 7A 04            [12] 1359 	mov	r2,#(_leds_off >> 16)
      00010F 12 08 14         [24] 1360 	lcall	__sdcc_banked_call
      000112 D0 02            [24] 1361 	pop	ar2
      000114 D0 03            [24] 1362 	pop	ar3
      000116 D0 04            [24] 1363 	pop	ar4
      000118 D0 05            [24] 1364 	pop	ar5
                                   1365 ;	../../platform/cc2530dk/./contiki-main.c:76: for(i = 0; i < 200 - j; ++i) {
      00011A E5 81            [12] 1366 	mov	a,sp
      00011C 24 FD            [12] 1367 	add	a,#0xfd
      00011E F8               [12] 1368 	mov	r0,a
      00011F E4               [12] 1369 	clr	a
      000120 F6               [12] 1370 	mov	@r0,a
      000121 08               [12] 1371 	inc	r0
      000122 F6               [12] 1372 	mov	@r0,a
      000123 74 C8            [12] 1373 	mov	a,#0xC8
      000125 C3               [12] 1374 	clr	c
      000126 9A               [12] 1375 	subb	a,r2
      000127 FE               [12] 1376 	mov	r6,a
      000128 E4               [12] 1377 	clr	a
      000129 9B               [12] 1378 	subb	a,r3
      00012A FF               [12] 1379 	mov	r7,a
      00012B                       1380 00108$:
      00012B E5 81            [12] 1381 	mov	a,sp
      00012D 24 FD            [12] 1382 	add	a,#0xfd
      00012F F8               [12] 1383 	mov	r0,a
      000130 C3               [12] 1384 	clr	c
      000131 E6               [12] 1385 	mov	a,@r0
      000132 9E               [12] 1386 	subb	a,r6
      000133 08               [12] 1387 	inc	r0
      000134 E6               [12] 1388 	mov	a,@r0
      000135 64 80            [12] 1389 	xrl	a,#0x80
      000137 8F F0            [24] 1390 	mov	b,r7
      000139 63 F0 80         [24] 1391 	xrl	b,#0x80
      00013C 95 F0            [12] 1392 	subb	a,b
      00013E 50 1D            [24] 1393 	jnc	00111$
                                   1394 ;	../../platform/cc2530dk/./contiki-main.c:77: a = i;
      000140 E5 81            [12] 1395 	mov	a,sp
      000142 24 FD            [12] 1396 	add	a,#0xfd
      000144 F8               [12] 1397 	mov	r0,a
      000145 A9 81            [24] 1398 	mov	r1,sp
      000147 19               [12] 1399 	dec	r1
      000148 E6               [12] 1400 	mov	a,@r0
      000149 F7               [12] 1401 	mov	@r1,a
      00014A 08               [12] 1402 	inc	r0
      00014B 09               [12] 1403 	inc	r1
      00014C E6               [12] 1404 	mov	a,@r0
      00014D F7               [12] 1405 	mov	@r1,a
                                   1406 ;	../../platform/cc2530dk/./contiki-main.c:76: for(i = 0; i < 200 - j; ++i) {
      00014E E5 81            [12] 1407 	mov	a,sp
      000150 24 FD            [12] 1408 	add	a,#0xfd
      000152 F8               [12] 1409 	mov	r0,a
      000153 74 01            [12] 1410 	mov	a,#0x01
      000155 26               [12] 1411 	add	a,@r0
      000156 F6               [12] 1412 	mov	@r0,a
      000157 E4               [12] 1413 	clr	a
      000158 08               [12] 1414 	inc	r0
      000159 36               [12] 1415 	addc	a,@r0
      00015A F6               [12] 1416 	mov	@r0,a
      00015B 80 CE            [24] 1417 	sjmp	00108$
      00015D                       1418 00111$:
                                   1419 ;	../../platform/cc2530dk/./contiki-main.c:68: for(k = 0; k < 400; ++k) {
      00015D 0C               [12] 1420 	inc	r4
      00015E BC 00 01         [24] 1421 	cjne	r4,#0x00,00138$
      000161 0D               [12] 1422 	inc	r5
      000162                       1423 00138$:
      000162 C3               [12] 1424 	clr	c
      000163 EC               [12] 1425 	mov	a,r4
      000164 94 90            [12] 1426 	subb	a,#0x90
      000166 ED               [12] 1427 	mov	a,r5
      000167 64 80            [12] 1428 	xrl	a,#0x80
      000169 94 81            [12] 1429 	subb	a,#0x81
      00016B 50 03            [24] 1430 	jnc	00139$
      00016D 02 00 7F         [24] 1431 	ljmp	00110$
      000170                       1432 00139$:
      000170 E5 81            [12] 1433 	mov	a,sp
      000172 24 FA            [12] 1434 	add	a,#0xFA
      000174 F5 81            [12] 1435 	mov	sp,a
      000176 22               [24] 1436 	ret
                                   1437 ;------------------------------------------------------------
                                   1438 ;Allocation info for local variables in function 'set_rf_params'
                                   1439 ;------------------------------------------------------------
                                   1440 ;i                         Allocated to registers r4 
                                   1441 ;short_addr                Allocated to registers r7 r6 
                                   1442 ;ext_addr                  Allocated to stack - sp -7
                                   1443 ;macp                      Allocated to registers 
                                   1444 ;------------------------------------------------------------
                                   1445 ;	../../platform/cc2530dk/./contiki-main.c:83: set_rf_params(void) CC_NON_BANKED
                                   1446 ;	-----------------------------------------
                                   1447 ;	 function set_rf_params
                                   1448 ;	-----------------------------------------
      000177                       1449 _set_rf_params:
      000177 E5 81            [12] 1450 	mov	a,sp
      000179 24 08            [12] 1451 	add	a,#0x08
      00017B F5 81            [12] 1452 	mov	sp,a
                                   1453 ;	../../platform/cc2530dk/./contiki-main.c:90: __xdata unsigned char *macp = &X_IEEE_ADDR;
      00017D 7E 0C            [12] 1454 	mov	r6,#_X_IEEE_ADDR
      00017F 7F 78            [12] 1455 	mov	r7,#(_X_IEEE_ADDR >> 8)
                                   1456 ;	../../platform/cc2530dk/./contiki-main.c:124: for(i = 7; i >= 0; --i) {
      000181 E5 81            [12] 1457 	mov	a,sp
      000183 24 F9            [12] 1458 	add	a,#0xF9
      000185 FD               [12] 1459 	mov	r5,a
      000186 7C 07            [12] 1460 	mov	r4,#0x07
      000188                       1461 00102$:
                                   1462 ;	../../platform/cc2530dk/./contiki-main.c:125: ext_addr[i] = *macp;
      000188 EC               [12] 1463 	mov	a,r4
      000189 2D               [12] 1464 	add	a,r5
      00018A F9               [12] 1465 	mov	r1,a
      00018B 8E 82            [24] 1466 	mov	dpl,r6
      00018D 8F 83            [24] 1467 	mov	dph,r7
      00018F E0               [24] 1468 	movx	a,@dptr
      000190 FB               [12] 1469 	mov	r3,a
      000191 A3               [24] 1470 	inc	dptr
      000192 AE 82            [24] 1471 	mov	r6,dpl
      000194 AF 83            [24] 1472 	mov	r7,dph
      000196 A7 03            [24] 1473 	mov	@r1,ar3
                                   1474 ;	../../platform/cc2530dk/./contiki-main.c:126: macp++;
                                   1475 ;	../../platform/cc2530dk/./contiki-main.c:124: for(i = 7; i >= 0; --i) {
      000198 1C               [12] 1476 	dec	r4
      000199 EC               [12] 1477 	mov	a,r4
      00019A 30 E7 EB         [24] 1478 	jnb	acc.7,00102$
                                   1479 ;	../../platform/cc2530dk/./contiki-main.c:135: short_addr = ext_addr[7];
      00019D 74 07            [12] 1480 	mov	a,#0x07
      00019F 2D               [12] 1481 	add	a,r5
      0001A0 F9               [12] 1482 	mov	r1,a
      0001A1 87 07            [24] 1483 	mov	ar7,@r1
      0001A3 7E 00            [12] 1484 	mov	r6,#0x00
                                   1485 ;	../../platform/cc2530dk/./contiki-main.c:136: short_addr |= ext_addr[6] << 8;
      0001A5 74 06            [12] 1486 	mov	a,#0x06
      0001A7 2D               [12] 1487 	add	a,r5
      0001A8 F9               [12] 1488 	mov	r1,a
      0001A9 87 04            [24] 1489 	mov	ar4,@r1
      0001AB 8C 03            [24] 1490 	mov	ar3,r4
      0001AD E4               [12] 1491 	clr	a
      0001AE 42 07            [12] 1492 	orl	ar7,a
      0001B0 EB               [12] 1493 	mov	a,r3
      0001B1 42 06            [12] 1494 	orl	ar6,a
                                   1495 ;	../../platform/cc2530dk/./contiki-main.c:139: memcpy(&linkaddr_node_addr, &ext_addr[8 - LINKADDR_SIZE], LINKADDR_SIZE);
      0001B3 8D 04            [24] 1496 	mov	ar4,r5
      0001B5 7B 00            [12] 1497 	mov	r3,#0x00
      0001B7 7A 40            [12] 1498 	mov	r2,#0x40
      0001B9 C0 07            [24] 1499 	push	ar7
      0001BB C0 06            [24] 1500 	push	ar6
      0001BD C0 05            [24] 1501 	push	ar5
      0001BF 74 08            [12] 1502 	mov	a,#0x08
      0001C1 C0 E0            [24] 1503 	push	acc
      0001C3 E4               [12] 1504 	clr	a
      0001C4 C0 E0            [24] 1505 	push	acc
      0001C6 C0 04            [24] 1506 	push	ar4
      0001C8 C0 03            [24] 1507 	push	ar3
      0001CA C0 02            [24] 1508 	push	ar2
      0001CC 90 0C 5D         [24] 1509 	mov	dptr,#_linkaddr_node_addr
      0001CF 75 F0 00         [24] 1510 	mov	b,#0x00
      0001D2 78 9F            [12] 1511 	mov	r0,#_memcpy
      0001D4 79 57            [12] 1512 	mov	r1,#(_memcpy >> 8)
      0001D6 7A 00            [12] 1513 	mov	r2,#(_memcpy >> 16)
      0001D8 12 08 14         [24] 1514 	lcall	__sdcc_banked_call
      0001DB E5 81            [12] 1515 	mov	a,sp
      0001DD 24 FB            [12] 1516 	add	a,#0xfb
      0001DF F5 81            [12] 1517 	mov	sp,a
                                   1518 ;	../../platform/cc2530dk/./contiki-main.c:153: NETSTACK_RADIO.set_value(RADIO_PARAM_PAN_ID, IEEE802154_PANID);
      0001E1 90 7D 87         [24] 1519 	mov	dptr,#(_cc2530_rf_driver + 0x0021)
      0001E4 E4               [12] 1520 	clr	a
      0001E5 93               [24] 1521 	movc	a,@a+dptr
      0001E6 FA               [12] 1522 	mov	r2,a
      0001E7 A3               [24] 1523 	inc	dptr
      0001E8 E4               [12] 1524 	clr	a
      0001E9 93               [24] 1525 	movc	a,@a+dptr
      0001EA FB               [12] 1526 	mov	r3,a
      0001EB A3               [24] 1527 	inc	dptr
      0001EC E4               [12] 1528 	clr	a
      0001ED 93               [24] 1529 	movc	a,@a+dptr
      0001EE FC               [12] 1530 	mov	r4,a
      0001EF C0 04            [24] 1531 	push	ar4
      0001F1 C0 03            [24] 1532 	push	ar3
      0001F3 C0 02            [24] 1533 	push	ar2
      0001F5 74 CD            [12] 1534 	mov	a,#0xCD
      0001F7 C0 E0            [24] 1535 	push	acc
      0001F9 74 AB            [12] 1536 	mov	a,#0xAB
      0001FB C0 E0            [24] 1537 	push	acc
      0001FD C0 02            [24] 1538 	push	ar2
      0001FF C0 03            [24] 1539 	push	ar3
      000201 C0 04            [24] 1540 	push	ar4
      000203 90 00 02         [24] 1541 	mov	dptr,#0x0002
      000206 D0 02            [24] 1542 	pop	ar2
      000208 D0 01            [24] 1543 	pop	ar1
      00020A D0 00            [24] 1544 	pop	ar0
      00020C 12 08 14         [24] 1545 	lcall	__sdcc_banked_call
      00020F 15 81            [12] 1546 	dec	sp
      000211 15 81            [12] 1547 	dec	sp
      000213 D0 02            [24] 1548 	pop	ar2
      000215 D0 03            [24] 1549 	pop	ar3
      000217 D0 04            [24] 1550 	pop	ar4
      000219 D0 05            [24] 1551 	pop	ar5
      00021B D0 06            [24] 1552 	pop	ar6
      00021D D0 07            [24] 1553 	pop	ar7
                                   1554 ;	../../platform/cc2530dk/./contiki-main.c:154: NETSTACK_RADIO.set_value(RADIO_PARAM_16BIT_ADDR, short_addr);
      00021F 90 7D 87         [24] 1555 	mov	dptr,#(_cc2530_rf_driver + 0x0021)
      000222 E4               [12] 1556 	clr	a
      000223 93               [24] 1557 	movc	a,@a+dptr
      000224 FA               [12] 1558 	mov	r2,a
      000225 A3               [24] 1559 	inc	dptr
      000226 E4               [12] 1560 	clr	a
      000227 93               [24] 1561 	movc	a,@a+dptr
      000228 FB               [12] 1562 	mov	r3,a
      000229 A3               [24] 1563 	inc	dptr
      00022A E4               [12] 1564 	clr	a
      00022B 93               [24] 1565 	movc	a,@a+dptr
      00022C FC               [12] 1566 	mov	r4,a
      00022D C0 05            [24] 1567 	push	ar5
      00022F C0 04            [24] 1568 	push	ar4
      000231 C0 03            [24] 1569 	push	ar3
      000233 C0 02            [24] 1570 	push	ar2
      000235 C0 07            [24] 1571 	push	ar7
      000237 C0 06            [24] 1572 	push	ar6
      000239 C0 02            [24] 1573 	push	ar2
      00023B C0 03            [24] 1574 	push	ar3
      00023D C0 04            [24] 1575 	push	ar4
      00023F 90 00 03         [24] 1576 	mov	dptr,#0x0003
      000242 D0 02            [24] 1577 	pop	ar2
      000244 D0 01            [24] 1578 	pop	ar1
      000246 D0 00            [24] 1579 	pop	ar0
      000248 12 08 14         [24] 1580 	lcall	__sdcc_banked_call
      00024B 15 81            [12] 1581 	dec	sp
      00024D 15 81            [12] 1582 	dec	sp
      00024F D0 02            [24] 1583 	pop	ar2
      000251 D0 03            [24] 1584 	pop	ar3
      000253 D0 04            [24] 1585 	pop	ar4
      000255 D0 05            [24] 1586 	pop	ar5
                                   1587 ;	../../platform/cc2530dk/./contiki-main.c:155: NETSTACK_RADIO.set_value(RADIO_PARAM_CHANNEL, CC2530_RF_CHANNEL);
      000257 90 7D 87         [24] 1588 	mov	dptr,#(_cc2530_rf_driver + 0x0021)
      00025A E4               [12] 1589 	clr	a
      00025B 93               [24] 1590 	movc	a,@a+dptr
      00025C FC               [12] 1591 	mov	r4,a
      00025D A3               [24] 1592 	inc	dptr
      00025E E4               [12] 1593 	clr	a
      00025F 93               [24] 1594 	movc	a,@a+dptr
      000260 FE               [12] 1595 	mov	r6,a
      000261 A3               [24] 1596 	inc	dptr
      000262 E4               [12] 1597 	clr	a
      000263 93               [24] 1598 	movc	a,@a+dptr
      000264 FF               [12] 1599 	mov	r7,a
      000265 C0 07            [24] 1600 	push	ar7
      000267 C0 06            [24] 1601 	push	ar6
      000269 C0 05            [24] 1602 	push	ar5
      00026B C0 04            [24] 1603 	push	ar4
      00026D 74 19            [12] 1604 	mov	a,#0x19
      00026F C0 E0            [24] 1605 	push	acc
      000271 E4               [12] 1606 	clr	a
      000272 C0 E0            [24] 1607 	push	acc
      000274 C0 04            [24] 1608 	push	ar4
      000276 C0 06            [24] 1609 	push	ar6
      000278 C0 07            [24] 1610 	push	ar7
      00027A 90 00 01         [24] 1611 	mov	dptr,#0x0001
      00027D D0 02            [24] 1612 	pop	ar2
      00027F D0 01            [24] 1613 	pop	ar1
      000281 D0 00            [24] 1614 	pop	ar0
      000283 12 08 14         [24] 1615 	lcall	__sdcc_banked_call
      000286 15 81            [12] 1616 	dec	sp
      000288 15 81            [12] 1617 	dec	sp
      00028A D0 04            [24] 1618 	pop	ar4
      00028C D0 05            [24] 1619 	pop	ar5
      00028E D0 06            [24] 1620 	pop	ar6
      000290 D0 07            [24] 1621 	pop	ar7
                                   1622 ;	../../platform/cc2530dk/./contiki-main.c:156: NETSTACK_RADIO.set_object(RADIO_PARAM_64BIT_ADDR, ext_addr, 8);
      000292 90 7D 8D         [24] 1623 	mov	dptr,#(_cc2530_rf_driver + 0x0027)
      000295 E4               [12] 1624 	clr	a
      000296 93               [24] 1625 	movc	a,@a+dptr
      000297 FC               [12] 1626 	mov	r4,a
      000298 A3               [24] 1627 	inc	dptr
      000299 E4               [12] 1628 	clr	a
      00029A 93               [24] 1629 	movc	a,@a+dptr
      00029B FE               [12] 1630 	mov	r6,a
      00029C A3               [24] 1631 	inc	dptr
      00029D E4               [12] 1632 	clr	a
      00029E 93               [24] 1633 	movc	a,@a+dptr
      00029F FF               [12] 1634 	mov	r7,a
      0002A0 7B 00            [12] 1635 	mov	r3,#0x00
      0002A2 7A 40            [12] 1636 	mov	r2,#0x40
      0002A4 C0 07            [24] 1637 	push	ar7
      0002A6 C0 06            [24] 1638 	push	ar6
      0002A8 C0 04            [24] 1639 	push	ar4
      0002AA 74 08            [12] 1640 	mov	a,#0x08
      0002AC C0 E0            [24] 1641 	push	acc
      0002AE E4               [12] 1642 	clr	a
      0002AF C0 E0            [24] 1643 	push	acc
      0002B1 C0 05            [24] 1644 	push	ar5
      0002B3 C0 03            [24] 1645 	push	ar3
      0002B5 C0 02            [24] 1646 	push	ar2
      0002B7 C0 04            [24] 1647 	push	ar4
      0002B9 C0 06            [24] 1648 	push	ar6
      0002BB C0 07            [24] 1649 	push	ar7
      0002BD 90 00 09         [24] 1650 	mov	dptr,#0x0009
      0002C0 D0 02            [24] 1651 	pop	ar2
      0002C2 D0 01            [24] 1652 	pop	ar1
      0002C4 D0 00            [24] 1653 	pop	ar0
      0002C6 12 08 14         [24] 1654 	lcall	__sdcc_banked_call
      0002C9 E5 81            [12] 1655 	mov	a,sp
      0002CB 24 FB            [12] 1656 	add	a,#0xfb
      0002CD F5 81            [12] 1657 	mov	sp,a
      0002CF D0 04            [24] 1658 	pop	ar4
      0002D1 D0 06            [24] 1659 	pop	ar6
      0002D3 D0 07            [24] 1660 	pop	ar7
                                   1661 ;	../../platform/cc2530dk/./contiki-main.c:157: return;
      0002D5 E5 81            [12] 1662 	mov	a,sp
      0002D7 24 F8            [12] 1663 	add	a,#0xF8
      0002D9 F5 81            [12] 1664 	mov	sp,a
      0002DB 22               [24] 1665 	ret
                                   1666 ;------------------------------------------------------------
                                   1667 ;Allocation info for local variables in function 'main'
                                   1668 ;------------------------------------------------------------
                                   1669 ;r                         Allocated to registers r6 
                                   1670 ;------------------------------------------------------------
                                   1671 ;	../../platform/cc2530dk/./contiki-main.c:161: main(void) CC_NON_BANKED
                                   1672 ;	-----------------------------------------
                                   1673 ;	 function main
                                   1674 ;	-----------------------------------------
      0002DC                       1675 _main:
                                   1676 ;	../../platform/cc2530dk/./contiki-main.c:164: clock_init();
      0002DC 78 B2            [12] 1677 	mov	r0,#_clock_init
      0002DE 79 08            [12] 1678 	mov	r1,#(_clock_init >> 8)
      0002E0 7A 00            [12] 1679 	mov	r2,#(_clock_init >> 16)
      0002E2 12 08 14         [24] 1680 	lcall	__sdcc_banked_call
                                   1681 ;	../../platform/cc2530dk/./contiki-main.c:165: soc_init();
      0002E5 78 F3            [12] 1682 	mov	r0,#_soc_init
      0002E7 79 B6            [12] 1683 	mov	r1,#(_soc_init >> 8)
      0002E9 7A 02            [12] 1684 	mov	r2,#(_soc_init >> 16)
      0002EB 12 08 14         [24] 1685 	lcall	__sdcc_banked_call
                                   1686 ;	../../platform/cc2530dk/./contiki-main.c:166: rtimer_init();
      0002EE 78 53            [12] 1687 	mov	r0,#_rtimer_init
      0002F0 79 81            [12] 1688 	mov	r1,#(_rtimer_init >> 8)
      0002F2 7A 04            [12] 1689 	mov	r2,#(_rtimer_init >> 16)
      0002F4 12 08 14         [24] 1690 	lcall	__sdcc_banked_call
                                   1691 ;	../../platform/cc2530dk/./contiki-main.c:171: leds_init();
      0002F7 78 B5            [12] 1692 	mov	r0,#_leds_init
      0002F9 79 80            [12] 1693 	mov	r1,#(_leds_init >> 8)
      0002FB 7A 04            [12] 1694 	mov	r2,#(_leds_init >> 16)
      0002FD 12 08 14         [24] 1695 	lcall	__sdcc_banked_call
                                   1696 ;	../../platform/cc2530dk/./contiki-main.c:172: leds_off(LEDS_ALL);
      000300 75 82 07         [24] 1697 	mov	dpl,#0x07
      000303 78 25            [12] 1698 	mov	r0,#_leds_off
      000305 79 81            [12] 1699 	mov	r1,#(_leds_off >> 8)
      000307 7A 04            [12] 1700 	mov	r2,#(_leds_off >> 16)
      000309 12 08 14         [24] 1701 	lcall	__sdcc_banked_call
                                   1702 ;	../../platform/cc2530dk/./contiki-main.c:173: fade(LEDS_GREEN);
      00030C 90 00 01         [24] 1703 	mov	dptr,#0x0001
      00030F 12 00 71         [24] 1704 	lcall	_fade
                                   1705 ;	../../platform/cc2530dk/./contiki-main.c:176: process_init();
      000312 78 E2            [12] 1706 	mov	r0,#_process_init
      000314 79 90            [12] 1707 	mov	r1,#(_process_init >> 8)
      000316 7A 03            [12] 1708 	mov	r2,#(_process_init >> 16)
      000318 12 08 14         [24] 1709 	lcall	__sdcc_banked_call
                                   1710 ;	../../platform/cc2530dk/./contiki-main.c:182: io_arch_init();
      00031B 78 E9            [12] 1711 	mov	r0,#_uart0_init
      00031D 79 99            [12] 1712 	mov	r1,#(_uart0_init >> 8)
      00031F 7A 04            [12] 1713 	mov	r2,#(_uart0_init >> 16)
      000321 12 08 14         [24] 1714 	lcall	__sdcc_banked_call
                                   1715 ;	../../platform/cc2530dk/./contiki-main.c:187: io_arch_set_input(serial_line_input_byte);
      000324 90 82 F3         [24] 1716 	mov	dptr,#_serial_line_input_byte
      000327 75 F0 04         [24] 1717 	mov	b,#(_serial_line_input_byte >> 16)
      00032A 78 01            [12] 1718 	mov	r0,#_uart0_set_input
      00032C 79 08            [12] 1719 	mov	r1,#(_uart0_set_input >> 8)
      00032E 7A 00            [12] 1720 	mov	r2,#(_uart0_set_input >> 16)
      000330 12 08 14         [24] 1721 	lcall	__sdcc_banked_call
                                   1722 ;	../../platform/cc2530dk/./contiki-main.c:188: serial_line_init();
      000333 78 28            [12] 1723 	mov	r0,#_serial_line_init
      000335 79 85            [12] 1724 	mov	r1,#(_serial_line_init >> 8)
      000337 7A 04            [12] 1725 	mov	r2,#(_serial_line_init >> 16)
      000339 12 08 14         [24] 1726 	lcall	__sdcc_banked_call
                                   1727 ;	../../platform/cc2530dk/./contiki-main.c:190: fade(LEDS_RED);
      00033C 90 00 02         [24] 1728 	mov	dptr,#0x0002
      00033F 12 00 71         [24] 1729 	lcall	_fade
                                   1730 ;	../../platform/cc2530dk/./contiki-main.c:193: putstring(CONTIKI_VERSION_STRING "\n");
      000342 90 7C 9D         [24] 1731 	mov	dptr,#__str_0
      000345 75 F0 80         [24] 1732 	mov	b,#0x80
      000348 78 6E            [12] 1733 	mov	r0,#_putstring
      00034A 79 8A            [12] 1734 	mov	r1,#(_putstring >> 8)
      00034C 7A 04            [12] 1735 	mov	r2,#(_putstring >> 16)
      00034E 12 08 14         [24] 1736 	lcall	__sdcc_banked_call
                                   1737 ;	../../platform/cc2530dk/./contiki-main.c:194: putstring(MODEL_STRING);
      000351 90 7C AA         [24] 1738 	mov	dptr,#__str_1
      000354 75 F0 80         [24] 1739 	mov	b,#0x80
      000357 78 6E            [12] 1740 	mov	r0,#_putstring
      000359 79 8A            [12] 1741 	mov	r1,#(_putstring >> 8)
      00035B 7A 04            [12] 1742 	mov	r2,#(_putstring >> 16)
      00035D 12 08 14         [24] 1743 	lcall	__sdcc_banked_call
                                   1744 ;	../../platform/cc2530dk/./contiki-main.c:195: switch(CHIPID) {
      000360 90 62 4A         [24] 1745 	mov	dptr,#_CHIPID
      000363 E0               [24] 1746 	movx	a,@dptr
      000364 FF               [12] 1747 	mov	r7,a
      000365 BF 8D 02         [24] 1748 	cjne	r7,#0x8D,00158$
      000368 80 42            [24] 1749 	sjmp	00104$
      00036A                       1750 00158$:
      00036A BF 95 02         [24] 1751 	cjne	r7,#0x95,00159$
      00036D 80 2C            [24] 1752 	sjmp	00103$
      00036F                       1753 00159$:
      00036F BF A5 02         [24] 1754 	cjne	r7,#0xA5,00160$
      000372 80 05            [24] 1755 	sjmp	00101$
      000374                       1756 00160$:
                                   1757 ;	../../platform/cc2530dk/./contiki-main.c:196: case 0xA5:
      000374 BF B5 44         [24] 1758 	cjne	r7,#0xB5,00105$
      000377 80 11            [24] 1759 	sjmp	00102$
      000379                       1760 00101$:
                                   1761 ;	../../platform/cc2530dk/./contiki-main.c:197: putstring("cc2530");
      000379 90 7C BB         [24] 1762 	mov	dptr,#__str_2
      00037C 75 F0 80         [24] 1763 	mov	b,#0x80
      00037F 78 6E            [12] 1764 	mov	r0,#_putstring
      000381 79 8A            [12] 1765 	mov	r1,#(_putstring >> 8)
      000383 7A 04            [12] 1766 	mov	r2,#(_putstring >> 16)
      000385 12 08 14         [24] 1767 	lcall	__sdcc_banked_call
                                   1768 ;	../../platform/cc2530dk/./contiki-main.c:198: break;
                                   1769 ;	../../platform/cc2530dk/./contiki-main.c:199: case 0xB5:
      000388 80 31            [24] 1770 	sjmp	00105$
      00038A                       1771 00102$:
                                   1772 ;	../../platform/cc2530dk/./contiki-main.c:200: putstring("cc2531");
      00038A 90 7C C2         [24] 1773 	mov	dptr,#__str_3
      00038D 75 F0 80         [24] 1774 	mov	b,#0x80
      000390 78 6E            [12] 1775 	mov	r0,#_putstring
      000392 79 8A            [12] 1776 	mov	r1,#(_putstring >> 8)
      000394 7A 04            [12] 1777 	mov	r2,#(_putstring >> 16)
      000396 12 08 14         [24] 1778 	lcall	__sdcc_banked_call
                                   1779 ;	../../platform/cc2530dk/./contiki-main.c:201: break;
                                   1780 ;	../../platform/cc2530dk/./contiki-main.c:202: case 0x95:
      000399 80 20            [24] 1781 	sjmp	00105$
      00039B                       1782 00103$:
                                   1783 ;	../../platform/cc2530dk/./contiki-main.c:203: putstring("cc2533");
      00039B 90 7C C9         [24] 1784 	mov	dptr,#__str_4
      00039E 75 F0 80         [24] 1785 	mov	b,#0x80
      0003A1 78 6E            [12] 1786 	mov	r0,#_putstring
      0003A3 79 8A            [12] 1787 	mov	r1,#(_putstring >> 8)
      0003A5 7A 04            [12] 1788 	mov	r2,#(_putstring >> 16)
      0003A7 12 08 14         [24] 1789 	lcall	__sdcc_banked_call
                                   1790 ;	../../platform/cc2530dk/./contiki-main.c:204: break;
                                   1791 ;	../../platform/cc2530dk/./contiki-main.c:205: case 0x8D:
      0003AA 80 0F            [24] 1792 	sjmp	00105$
      0003AC                       1793 00104$:
                                   1794 ;	../../platform/cc2530dk/./contiki-main.c:206: putstring("cc2540");
      0003AC 90 7C D0         [24] 1795 	mov	dptr,#__str_5
      0003AF 75 F0 80         [24] 1796 	mov	b,#0x80
      0003B2 78 6E            [12] 1797 	mov	r0,#_putstring
      0003B4 79 8A            [12] 1798 	mov	r1,#(_putstring >> 8)
      0003B6 7A 04            [12] 1799 	mov	r2,#(_putstring >> 16)
      0003B8 12 08 14         [24] 1800 	lcall	__sdcc_banked_call
                                   1801 ;	../../platform/cc2530dk/./contiki-main.c:208: }
      0003BB                       1802 00105$:
                                   1803 ;	../../platform/cc2530dk/./contiki-main.c:210: putstring("-" CC2530_FLAVOR_STRING ", ");
      0003BB 90 7C D7         [24] 1804 	mov	dptr,#__str_6
      0003BE 75 F0 80         [24] 1805 	mov	b,#0x80
      0003C1 78 6E            [12] 1806 	mov	r0,#_putstring
      0003C3 79 8A            [12] 1807 	mov	r1,#(_putstring >> 8)
      0003C5 7A 04            [12] 1808 	mov	r2,#(_putstring >> 16)
      0003C7 12 08 14         [24] 1809 	lcall	__sdcc_banked_call
                                   1810 ;	../../platform/cc2530dk/./contiki-main.c:211: puthex(CHIPINFO1 + 1);
      0003CA 90 62 77         [24] 1811 	mov	dptr,#_CHIPINFO1
      0003CD E0               [24] 1812 	movx	a,@dptr
      0003CE FF               [12] 1813 	mov	r7,a
      0003CF 0F               [12] 1814 	inc	r7
      0003D0 8F 82            [24] 1815 	mov	dpl,r7
      0003D2 78 A1            [12] 1816 	mov	r0,#_puthex
      0003D4 79 8A            [12] 1817 	mov	r1,#(_puthex >> 8)
      0003D6 7A 04            [12] 1818 	mov	r2,#(_puthex >> 16)
      0003D8 12 08 14         [24] 1819 	lcall	__sdcc_banked_call
                                   1820 ;	../../platform/cc2530dk/./contiki-main.c:212: putstring("KB SRAM\n");
      0003DB 90 7C DF         [24] 1821 	mov	dptr,#__str_7
      0003DE 75 F0 80         [24] 1822 	mov	b,#0x80
      0003E1 78 6E            [12] 1823 	mov	r0,#_putstring
      0003E3 79 8A            [12] 1824 	mov	r1,#(_putstring >> 8)
      0003E5 7A 04            [12] 1825 	mov	r2,#(_putstring >> 16)
      0003E7 12 08 14         [24] 1826 	lcall	__sdcc_banked_call
                                   1827 ;	../../platform/cc2530dk/./contiki-main.c:244: watchdog_init();
      0003EA 78 73            [12] 1828 	mov	r0,#_watchdog_init
      0003EC 79 80            [12] 1829 	mov	r1,#(_watchdog_init >> 8)
      0003EE 7A 04            [12] 1830 	mov	r2,#(_watchdog_init >> 16)
      0003F0 12 08 14         [24] 1831 	lcall	__sdcc_banked_call
                                   1832 ;	../../platform/cc2530dk/./contiki-main.c:247: random_init(0);
      0003F3 90 00 00         [24] 1833 	mov	dptr,#0x0000
      0003F6 78 A2            [12] 1834 	mov	r0,#_random_init
      0003F8 79 A0            [12] 1835 	mov	r1,#(_random_init >> 8)
      0003FA 7A 04            [12] 1836 	mov	r2,#(_random_init >> 16)
      0003FC 12 08 14         [24] 1837 	lcall	__sdcc_banked_call
                                   1838 ;	../../platform/cc2530dk/./contiki-main.c:250: process_start(&etimer_process, NULL);
      0003FF E4               [12] 1839 	clr	a
      000400 C0 E0            [24] 1840 	push	acc
      000402 C0 E0            [24] 1841 	push	acc
      000404 C0 E0            [24] 1842 	push	acc
      000406 90 0F B6         [24] 1843 	mov	dptr,#_etimer_process
      000409 75 F0 00         [24] 1844 	mov	b,#0x00
      00040C 78 AD            [12] 1845 	mov	r0,#_process_start
      00040E 79 8A            [12] 1846 	mov	r1,#(_process_start >> 8)
      000410 7A 03            [12] 1847 	mov	r2,#(_process_start >> 16)
      000412 12 08 14         [24] 1848 	lcall	__sdcc_banked_call
      000415 15 81            [12] 1849 	dec	sp
      000417 15 81            [12] 1850 	dec	sp
      000419 15 81            [12] 1851 	dec	sp
                                   1852 ;	../../platform/cc2530dk/./contiki-main.c:251: ctimer_init();
      00041B 78 38            [12] 1853 	mov	r0,#_ctimer_init
      00041D 79 E6            [12] 1854 	mov	r1,#(_ctimer_init >> 8)
      00041F 7A 03            [12] 1855 	mov	r2,#(_ctimer_init >> 16)
      000421 12 08 14         [24] 1856 	lcall	__sdcc_banked_call
                                   1857 ;	../../platform/cc2530dk/./contiki-main.c:254: netstack_init();
      000424 78 45            [12] 1858 	mov	r0,#_netstack_init
      000426 79 8B            [12] 1859 	mov	r1,#(_netstack_init >> 8)
      000428 7A 04            [12] 1860 	mov	r2,#(_netstack_init >> 16)
      00042A 12 08 14         [24] 1861 	lcall	__sdcc_banked_call
                                   1862 ;	../../platform/cc2530dk/./contiki-main.c:255: set_rf_params();
      00042D 12 01 77         [24] 1863 	lcall	_set_rf_params
                                   1864 ;	../../platform/cc2530dk/./contiki-main.c:258: process_start(&sensors_process, NULL);
      000430 E4               [12] 1865 	clr	a
      000431 C0 E0            [24] 1866 	push	acc
      000433 C0 E0            [24] 1867 	push	acc
      000435 C0 E0            [24] 1868 	push	acc
      000437 90 0F D0         [24] 1869 	mov	dptr,#_sensors_process
      00043A 75 F0 00         [24] 1870 	mov	b,#0x00
      00043D 78 AD            [12] 1871 	mov	r0,#_process_start
      00043F 79 8A            [12] 1872 	mov	r1,#(_process_start >> 8)
      000441 7A 03            [12] 1873 	mov	r2,#(_process_start >> 16)
      000443 12 08 14         [24] 1874 	lcall	__sdcc_banked_call
      000446 15 81            [12] 1875 	dec	sp
      000448 15 81            [12] 1876 	dec	sp
      00044A 15 81            [12] 1877 	dec	sp
                                   1878 ;	../../platform/cc2530dk/./contiki-main.c:259: BUTTON_SENSOR_ACTIVATE();
      00044C 90 7D 12         [24] 1879 	mov	dptr,#(_button_1_sensor + 0x0006)
      00044F E4               [12] 1880 	clr	a
      000450 93               [24] 1881 	movc	a,@a+dptr
      000451 FD               [12] 1882 	mov	r5,a
      000452 A3               [24] 1883 	inc	dptr
      000453 E4               [12] 1884 	clr	a
      000454 93               [24] 1885 	movc	a,@a+dptr
      000455 FE               [12] 1886 	mov	r6,a
      000456 A3               [24] 1887 	inc	dptr
      000457 E4               [12] 1888 	clr	a
      000458 93               [24] 1889 	movc	a,@a+dptr
      000459 FF               [12] 1890 	mov	r7,a
      00045A C0 07            [24] 1891 	push	ar7
      00045C C0 06            [24] 1892 	push	ar6
      00045E C0 05            [24] 1893 	push	ar5
      000460 74 01            [12] 1894 	mov	a,#0x01
      000462 C0 E0            [24] 1895 	push	acc
      000464 E4               [12] 1896 	clr	a
      000465 C0 E0            [24] 1897 	push	acc
      000467 C0 05            [24] 1898 	push	ar5
      000469 C0 06            [24] 1899 	push	ar6
      00046B C0 07            [24] 1900 	push	ar7
      00046D 90 00 81         [24] 1901 	mov	dptr,#0x0081
      000470 D0 02            [24] 1902 	pop	ar2
      000472 D0 01            [24] 1903 	pop	ar1
      000474 D0 00            [24] 1904 	pop	ar0
      000476 12 08 14         [24] 1905 	lcall	__sdcc_banked_call
      000479 15 81            [12] 1906 	dec	sp
      00047B 15 81            [12] 1907 	dec	sp
      00047D D0 05            [24] 1908 	pop	ar5
      00047F D0 06            [24] 1909 	pop	ar6
      000481 D0 07            [24] 1910 	pop	ar7
                                   1911 ;	../../platform/cc2530dk/./contiki-main.c:260: ADC_SENSOR_ACTIVATE();
      000483 90 7D 02         [24] 1912 	mov	dptr,#(_adc_sensor + 0x0006)
      000486 E4               [12] 1913 	clr	a
      000487 93               [24] 1914 	movc	a,@a+dptr
      000488 FD               [12] 1915 	mov	r5,a
      000489 A3               [24] 1916 	inc	dptr
      00048A E4               [12] 1917 	clr	a
      00048B 93               [24] 1918 	movc	a,@a+dptr
      00048C FE               [12] 1919 	mov	r6,a
      00048D A3               [24] 1920 	inc	dptr
      00048E E4               [12] 1921 	clr	a
      00048F 93               [24] 1922 	movc	a,@a+dptr
      000490 FF               [12] 1923 	mov	r7,a
      000491 C0 07            [24] 1924 	push	ar7
      000493 C0 06            [24] 1925 	push	ar6
      000495 C0 05            [24] 1926 	push	ar5
      000497 74 01            [12] 1927 	mov	a,#0x01
      000499 C0 E0            [24] 1928 	push	acc
      00049B E4               [12] 1929 	clr	a
      00049C C0 E0            [24] 1930 	push	acc
      00049E C0 05            [24] 1931 	push	ar5
      0004A0 C0 06            [24] 1932 	push	ar6
      0004A2 C0 07            [24] 1933 	push	ar7
      0004A4 90 00 81         [24] 1934 	mov	dptr,#0x0081
      0004A7 D0 02            [24] 1935 	pop	ar2
      0004A9 D0 01            [24] 1936 	pop	ar1
      0004AB D0 00            [24] 1937 	pop	ar0
      0004AD 12 08 14         [24] 1938 	lcall	__sdcc_banked_call
      0004B0 15 81            [12] 1939 	dec	sp
      0004B2 15 81            [12] 1940 	dec	sp
      0004B4 D0 05            [24] 1941 	pop	ar5
      0004B6 D0 06            [24] 1942 	pop	ar6
      0004B8 D0 07            [24] 1943 	pop	ar7
                                   1944 ;	../../platform/cc2530dk/./contiki-main.c:264: memcpy(&uip_lladdr.addr, &linkaddr_node_addr, sizeof(uip_lladdr.addr));
      0004BA 74 08            [12] 1945 	mov	a,#0x08
      0004BC C0 E0            [24] 1946 	push	acc
      0004BE E4               [12] 1947 	clr	a
      0004BF C0 E0            [24] 1948 	push	acc
      0004C1 74 5D            [12] 1949 	mov	a,#_linkaddr_node_addr
      0004C3 C0 E0            [24] 1950 	push	acc
      0004C5 74 0C            [12] 1951 	mov	a,#(_linkaddr_node_addr >> 8)
      0004C7 C0 E0            [24] 1952 	push	acc
      0004C9 E4               [12] 1953 	clr	a
      0004CA C0 E0            [24] 1954 	push	acc
      0004CC 90 07 8C         [24] 1955 	mov	dptr,#_uip_lladdr
      0004CF 75 F0 00         [24] 1956 	mov	b,#0x00
      0004D2 78 9F            [12] 1957 	mov	r0,#_memcpy
      0004D4 79 57            [12] 1958 	mov	r1,#(_memcpy >> 8)
      0004D6 7A 00            [12] 1959 	mov	r2,#(_memcpy >> 16)
      0004D8 12 08 14         [24] 1960 	lcall	__sdcc_banked_call
      0004DB E5 81            [12] 1961 	mov	a,sp
      0004DD 24 FB            [12] 1962 	add	a,#0xfb
      0004DF F5 81            [12] 1963 	mov	sp,a
                                   1964 ;	../../platform/cc2530dk/./contiki-main.c:265: queuebuf_init();
      0004E1 78 15            [12] 1965 	mov	r0,#_queuebuf_init
      0004E3 79 8C            [12] 1966 	mov	r1,#(_queuebuf_init >> 8)
      0004E5 7A 04            [12] 1967 	mov	r2,#(_queuebuf_init >> 16)
      0004E7 12 08 14         [24] 1968 	lcall	__sdcc_banked_call
                                   1969 ;	../../platform/cc2530dk/./contiki-main.c:266: process_start(&tcpip_process, NULL);
      0004EA E4               [12] 1970 	clr	a
      0004EB C0 E0            [24] 1971 	push	acc
      0004ED C0 E0            [24] 1972 	push	acc
      0004EF C0 E0            [24] 1973 	push	acc
      0004F1 90 10 46         [24] 1974 	mov	dptr,#_tcpip_process
      0004F4 75 F0 00         [24] 1975 	mov	b,#0x00
      0004F7 78 AD            [12] 1976 	mov	r0,#_process_start
      0004F9 79 8A            [12] 1977 	mov	r1,#(_process_start >> 8)
      0004FB 7A 03            [12] 1978 	mov	r2,#(_process_start >> 16)
      0004FD 12 08 14         [24] 1979 	lcall	__sdcc_banked_call
      000500 15 81            [12] 1980 	dec	sp
      000502 15 81            [12] 1981 	dec	sp
      000504 15 81            [12] 1982 	dec	sp
                                   1983 ;	../../platform/cc2530dk/./contiki-main.c:270: process_start(&viztool_process, NULL);
      000506 E4               [12] 1984 	clr	a
      000507 C0 E0            [24] 1985 	push	acc
      000509 C0 E0            [24] 1986 	push	acc
      00050B C0 E0            [24] 1987 	push	acc
      00050D 90 0F EE         [24] 1988 	mov	dptr,#_viztool_process
      000510 75 F0 00         [24] 1989 	mov	b,#0x00
      000513 78 AD            [12] 1990 	mov	r0,#_process_start
      000515 79 8A            [12] 1991 	mov	r1,#(_process_start >> 8)
      000517 7A 03            [12] 1992 	mov	r2,#(_process_start >> 16)
      000519 12 08 14         [24] 1993 	lcall	__sdcc_banked_call
      00051C 15 81            [12] 1994 	dec	sp
      00051E 15 81            [12] 1995 	dec	sp
      000520 15 81            [12] 1996 	dec	sp
                                   1997 ;	../../platform/cc2530dk/./contiki-main.c:273: energest_init();
      000522 78 EF            [12] 1998 	mov	r0,#_energest_init
      000524 79 8B            [12] 1999 	mov	r1,#(_energest_init >> 8)
      000526 7A 04            [12] 2000 	mov	r2,#(_energest_init >> 16)
      000528 12 08 14         [24] 2001 	lcall	__sdcc_banked_call
                                   2002 ;	../../platform/cc2530dk/./contiki-main.c:276: autostart_start(autostart_processes);
      00052B 90 7C E8         [24] 2003 	mov	dptr,#_autostart_processes
      00052E 75 F0 80         [24] 2004 	mov	b,#0x80
      000531 78 51            [12] 2005 	mov	r0,#_autostart_start
      000533 79 80            [12] 2006 	mov	r1,#(_autostart_start >> 8)
      000535 7A 02            [12] 2007 	mov	r2,#(_autostart_start >> 16)
      000537 12 08 14         [24] 2008 	lcall	__sdcc_banked_call
                                   2009 ;	../../platform/cc2530dk/./contiki-main.c:278: watchdog_start();
      00053A 78 79            [12] 2010 	mov	r0,#_watchdog_start
      00053C 79 80            [12] 2011 	mov	r1,#(_watchdog_start >> 8)
      00053E 7A 04            [12] 2012 	mov	r2,#(_watchdog_start >> 16)
      000540 12 08 14         [24] 2013 	lcall	__sdcc_banked_call
                                   2014 ;	../../platform/cc2530dk/./contiki-main.c:280: fade(LEDS_YELLOW);
      000543 90 00 04         [24] 2015 	mov	dptr,#0x0004
      000546 12 00 71         [24] 2016 	lcall	_fade
                                   2017 ;	../../platform/cc2530dk/./contiki-main.c:284: do {
      000549                       2018 00113$:
                                   2019 ;	../../platform/cc2530dk/./contiki-main.c:286: watchdog_periodic();
      000549 78 7F            [12] 2020 	mov	r0,#_watchdog_periodic
      00054B 79 80            [12] 2021 	mov	r1,#(_watchdog_periodic >> 8)
      00054D 7A 04            [12] 2022 	mov	r2,#(_watchdog_periodic >> 16)
      00054F 12 08 14         [24] 2023 	lcall	__sdcc_banked_call
                                   2024 ;	../../platform/cc2530dk/./contiki-main.c:289: if(sleep_flag) {
      000552 90 07 8B         [24] 2025 	mov	dptr,#_sleep_flag
      000555 E0               [24] 2026 	movx	a,@dptr
      000556 FF               [12] 2027 	mov	r7,a
      000557 60 57            [24] 2028 	jz	00112$
                                   2029 ;	../../platform/cc2530dk/./contiki-main.c:290: if(etimer_pending() &&
      000559 78 E1            [12] 2030 	mov	r0,#_etimer_pending
      00055B 79 88            [12] 2031 	mov	r1,#(_etimer_pending >> 8)
      00055D 7A 03            [12] 2032 	mov	r2,#(_etimer_pending >> 16)
      00055F 12 08 14         [24] 2033 	lcall	__sdcc_banked_call
      000562 E5 82            [12] 2034 	mov	a,dpl
      000564 85 83 F0         [24] 2035 	mov	b,dph
      000567 45 F0            [12] 2036 	orl	a,b
      000569 60 40            [24] 2037 	jz	00109$
                                   2038 ;	../../platform/cc2530dk/./contiki-main.c:291: (etimer_next_expiration_time() - clock_time() - 1) > MAX_TICKS) {
      00056B 78 1D            [12] 2039 	mov	r0,#_etimer_next_expiration_time
      00056D 79 89            [12] 2040 	mov	r1,#(_etimer_next_expiration_time >> 8)
      00056F 7A 03            [12] 2041 	mov	r2,#(_etimer_next_expiration_time >> 16)
      000571 12 08 14         [24] 2042 	lcall	__sdcc_banked_call
      000574 AE 82            [24] 2043 	mov	r6,dpl
      000576 AF 83            [24] 2044 	mov	r7,dph
      000578 C0 07            [24] 2045 	push	ar7
      00057A C0 06            [24] 2046 	push	ar6
      00057C 78 97            [12] 2047 	mov	r0,#_clock_time
      00057E 79 08            [12] 2048 	mov	r1,#(_clock_time >> 8)
      000580 7A 00            [12] 2049 	mov	r2,#(_clock_time >> 16)
      000582 12 08 14         [24] 2050 	lcall	__sdcc_banked_call
      000585 AC 82            [24] 2051 	mov	r4,dpl
      000587 AD 83            [24] 2052 	mov	r5,dph
      000589 D0 06            [24] 2053 	pop	ar6
      00058B D0 07            [24] 2054 	pop	ar7
      00058D EE               [12] 2055 	mov	a,r6
      00058E C3               [12] 2056 	clr	c
      00058F 9C               [12] 2057 	subb	a,r4
      000590 FE               [12] 2058 	mov	r6,a
      000591 EF               [12] 2059 	mov	a,r7
      000592 9D               [12] 2060 	subb	a,r5
      000593 FF               [12] 2061 	mov	r7,a
      000594 1E               [12] 2062 	dec	r6
      000595 BE FF 01         [24] 2063 	cjne	r6,#0xFF,00164$
      000598 1F               [12] 2064 	dec	r7
      000599                       2065 00164$:
      000599 C3               [12] 2066 	clr	c
      00059A 74 FF            [12] 2067 	mov	a,#0xFF
      00059C 9E               [12] 2068 	subb	a,r6
      00059D 74 7F            [12] 2069 	mov	a,#0x7F
      00059F 9F               [12] 2070 	subb	a,r7
      0005A0 50 09            [24] 2071 	jnc	00109$
                                   2072 ;	../../platform/cc2530dk/./contiki-main.c:292: etimer_request_poll();
      0005A2 78 F6            [12] 2073 	mov	r0,#_etimer_request_poll
      0005A4 79 85            [12] 2074 	mov	r1,#(_etimer_request_poll >> 8)
      0005A6 7A 03            [12] 2075 	mov	r2,#(_etimer_request_poll >> 16)
      0005A8 12 08 14         [24] 2076 	lcall	__sdcc_banked_call
      0005AB                       2077 00109$:
                                   2078 ;	../../platform/cc2530dk/./contiki-main.c:294: sleep_flag = 0;
      0005AB 90 07 8B         [24] 2079 	mov	dptr,#_sleep_flag
      0005AE E4               [12] 2080 	clr	a
      0005AF F0               [24] 2081 	movx	@dptr,a
      0005B0                       2082 00112$:
                                   2083 ;	../../platform/cc2530dk/./contiki-main.c:297: r = process_run();
      0005B0 78 78            [12] 2084 	mov	r0,#_process_run
      0005B2 79 93            [12] 2085 	mov	r1,#(_process_run >> 8)
      0005B4 7A 03            [12] 2086 	mov	r2,#(_process_run >> 16)
      0005B6 12 08 14         [24] 2087 	lcall	__sdcc_banked_call
      0005B9 AE 82            [24] 2088 	mov	r6,dpl
      0005BB AF 83            [24] 2089 	mov	r7,dph
                                   2090 ;	../../platform/cc2530dk/./contiki-main.c:298: } while(r > 0);
      0005BD EE               [12] 2091 	mov	a,r6
      0005BE 70 89            [24] 2092 	jnz	00113$
                                   2093 ;	../../platform/cc2530dk/./contiki-main.c:299: len = NETSTACK_RADIO.pending_packet();
      0005C0 90 7D 7B         [24] 2094 	mov	dptr,#(_cc2530_rf_driver + 0x0015)
      0005C3 E4               [12] 2095 	clr	a
      0005C4 93               [24] 2096 	movc	a,@a+dptr
      0005C5 FD               [12] 2097 	mov	r5,a
      0005C6 A3               [24] 2098 	inc	dptr
      0005C7 E4               [12] 2099 	clr	a
      0005C8 93               [24] 2100 	movc	a,@a+dptr
      0005C9 FE               [12] 2101 	mov	r6,a
      0005CA A3               [24] 2102 	inc	dptr
      0005CB E4               [12] 2103 	clr	a
      0005CC 93               [24] 2104 	movc	a,@a+dptr
      0005CD FF               [12] 2105 	mov	r7,a
      0005CE C0 07            [24] 2106 	push	ar7
      0005D0 C0 06            [24] 2107 	push	ar6
      0005D2 C0 05            [24] 2108 	push	ar5
      0005D4 C0 05            [24] 2109 	push	ar5
      0005D6 C0 06            [24] 2110 	push	ar6
      0005D8 C0 07            [24] 2111 	push	ar7
      0005DA D0 02            [24] 2112 	pop	ar2
      0005DC D0 01            [24] 2113 	pop	ar1
      0005DE D0 00            [24] 2114 	pop	ar0
      0005E0 12 08 14         [24] 2115 	lcall	__sdcc_banked_call
      0005E3 85 82 08         [24] 2116 	mov	_len,dpl
      0005E6 85 83 09         [24] 2117 	mov	(_len + 1),dph
      0005E9 D0 05            [24] 2118 	pop	ar5
      0005EB D0 06            [24] 2119 	pop	ar6
      0005ED D0 07            [24] 2120 	pop	ar7
                                   2121 ;	../../platform/cc2530dk/./contiki-main.c:300: if(len) {
      0005EF E5 08            [12] 2122 	mov	a,_len
      0005F1 45 09            [12] 2123 	orl	a,(_len + 1)
      0005F3 70 03            [24] 2124 	jnz	00167$
      0005F5 02 05 49         [24] 2125 	ljmp	00113$
      0005F8                       2126 00167$:
                                   2127 ;	../../platform/cc2530dk/./contiki-main.c:301: packetbuf_clear();
      0005F8 78 42            [12] 2128 	mov	r0,#_packetbuf_clear
      0005FA 79 AD            [12] 2129 	mov	r1,#(_packetbuf_clear >> 8)
      0005FC 7A 03            [12] 2130 	mov	r2,#(_packetbuf_clear >> 16)
      0005FE 12 08 14         [24] 2131 	lcall	__sdcc_banked_call
                                   2132 ;	../../platform/cc2530dk/./contiki-main.c:302: len = NETSTACK_RADIO.read(packetbuf_dataptr(), PACKETBUF_SIZE);
      000601 90 7D 72         [24] 2133 	mov	dptr,#(_cc2530_rf_driver + 0x000c)
      000604 E4               [12] 2134 	clr	a
      000605 93               [24] 2135 	movc	a,@a+dptr
      000606 FD               [12] 2136 	mov	r5,a
      000607 A3               [24] 2137 	inc	dptr
      000608 E4               [12] 2138 	clr	a
      000609 93               [24] 2139 	movc	a,@a+dptr
      00060A FE               [12] 2140 	mov	r6,a
      00060B A3               [24] 2141 	inc	dptr
      00060C E4               [12] 2142 	clr	a
      00060D 93               [24] 2143 	movc	a,@a+dptr
      00060E FF               [12] 2144 	mov	r7,a
      00060F C0 07            [24] 2145 	push	ar7
      000611 C0 06            [24] 2146 	push	ar6
      000613 C0 05            [24] 2147 	push	ar5
      000615 78 21            [12] 2148 	mov	r0,#_packetbuf_dataptr
      000617 79 B1            [12] 2149 	mov	r1,#(_packetbuf_dataptr >> 8)
      000619 7A 03            [12] 2150 	mov	r2,#(_packetbuf_dataptr >> 16)
      00061B 12 08 14         [24] 2151 	lcall	__sdcc_banked_call
      00061E AA 82            [24] 2152 	mov	r2,dpl
      000620 AB 83            [24] 2153 	mov	r3,dph
      000622 AC F0            [24] 2154 	mov	r4,b
      000624 D0 05            [24] 2155 	pop	ar5
      000626 D0 06            [24] 2156 	pop	ar6
      000628 D0 07            [24] 2157 	pop	ar7
      00062A C0 07            [24] 2158 	push	ar7
      00062C C0 06            [24] 2159 	push	ar6
      00062E C0 05            [24] 2160 	push	ar5
      000630 74 80            [12] 2161 	mov	a,#0x80
      000632 C0 E0            [24] 2162 	push	acc
      000634 E4               [12] 2163 	clr	a
      000635 C0 E0            [24] 2164 	push	acc
      000637 C0 05            [24] 2165 	push	ar5
      000639 C0 06            [24] 2166 	push	ar6
      00063B C0 07            [24] 2167 	push	ar7
      00063D 8A 82            [24] 2168 	mov	dpl,r2
      00063F 8B 83            [24] 2169 	mov	dph,r3
      000641 8C F0            [24] 2170 	mov	b,r4
      000643 D0 02            [24] 2171 	pop	ar2
      000645 D0 01            [24] 2172 	pop	ar1
      000647 D0 00            [24] 2173 	pop	ar0
      000649 12 08 14         [24] 2174 	lcall	__sdcc_banked_call
      00064C 85 82 08         [24] 2175 	mov	_len,dpl
      00064F 85 83 09         [24] 2176 	mov	(_len + 1),dph
      000652 15 81            [12] 2177 	dec	sp
      000654 15 81            [12] 2178 	dec	sp
      000656 D0 05            [24] 2179 	pop	ar5
      000658 D0 06            [24] 2180 	pop	ar6
      00065A D0 07            [24] 2181 	pop	ar7
                                   2182 ;	../../platform/cc2530dk/./contiki-main.c:303: if(len > 0) {
      00065C E5 08            [12] 2183 	mov	a,_len
      00065E 45 09            [12] 2184 	orl	a,(_len + 1)
      000660 70 03            [24] 2185 	jnz	00168$
      000662 02 05 49         [24] 2186 	ljmp	00113$
      000665                       2187 00168$:
                                   2188 ;	../../platform/cc2530dk/./contiki-main.c:304: packetbuf_set_datalen(len);
      000665 85 08 82         [24] 2189 	mov	dpl,_len
      000668 85 09 83         [24] 2190 	mov	dph,(_len + 1)
      00066B 78 13            [12] 2191 	mov	r0,#_packetbuf_set_datalen
      00066D 79 B1            [12] 2192 	mov	r1,#(_packetbuf_set_datalen >> 8)
      00066F 7A 03            [12] 2193 	mov	r2,#(_packetbuf_set_datalen >> 16)
      000671 12 08 14         [24] 2194 	lcall	__sdcc_banked_call
                                   2195 ;	../../platform/cc2530dk/./contiki-main.c:305: NETSTACK_RDC.input();
      000674 90 7E 31         [24] 2196 	mov	dptr,#(_nullrdc_driver + 0x000c)
      000677 E4               [12] 2197 	clr	a
      000678 93               [24] 2198 	movc	a,@a+dptr
      000679 FD               [12] 2199 	mov	r5,a
      00067A A3               [24] 2200 	inc	dptr
      00067B E4               [12] 2201 	clr	a
      00067C 93               [24] 2202 	movc	a,@a+dptr
      00067D FE               [12] 2203 	mov	r6,a
      00067E A3               [24] 2204 	inc	dptr
      00067F E4               [12] 2205 	clr	a
      000680 93               [24] 2206 	movc	a,@a+dptr
      000681 FF               [12] 2207 	mov	r7,a
      000682 C0 07            [24] 2208 	push	ar7
      000684 C0 06            [24] 2209 	push	ar6
      000686 C0 05            [24] 2210 	push	ar5
      000688 C0 05            [24] 2211 	push	ar5
      00068A C0 06            [24] 2212 	push	ar6
      00068C C0 07            [24] 2213 	push	ar7
      00068E D0 02            [24] 2214 	pop	ar2
      000690 D0 01            [24] 2215 	pop	ar1
      000692 D0 00            [24] 2216 	pop	ar0
      000694 12 08 14         [24] 2217 	lcall	__sdcc_banked_call
      000697 D0 05            [24] 2218 	pop	ar5
      000699 D0 06            [24] 2219 	pop	ar6
      00069B D0 07            [24] 2220 	pop	ar7
      00069D 02 05 49         [24] 2221 	ljmp	00113$
                                   2222 	.area CSEG    (CODE)
                                   2223 	.area CONST   (CODE)
      007C9D                       2224 __str_0:
      007C9D 43 6F 6E 74 69 6B 69  2225 	.ascii "Contiki 3.0"
             20 33 2E 30
      007CA8 0A                    2226 	.db 0x0A
      007CA9 00                    2227 	.db 0x00
      007CAA                       2228 __str_1:
      007CAA 54 49 20 53 6D 61 72  2229 	.ascii "TI SmartRF05 EB"
             74 52 46 30 35 20 45
             42
      007CB9 0A                    2230 	.db 0x0A
      007CBA 00                    2231 	.db 0x00
      007CBB                       2232 __str_2:
      007CBB 63 63 32 35 33 30     2233 	.ascii "cc2530"
      007CC1 00                    2234 	.db 0x00
      007CC2                       2235 __str_3:
      007CC2 63 63 32 35 33 31     2236 	.ascii "cc2531"
      007CC8 00                    2237 	.db 0x00
      007CC9                       2238 __str_4:
      007CC9 63 63 32 35 33 33     2239 	.ascii "cc2533"
      007CCF 00                    2240 	.db 0x00
      007CD0                       2241 __str_5:
      007CD0 63 63 32 35 34 30     2242 	.ascii "cc2540"
      007CD6 00                    2243 	.db 0x00
      007CD7                       2244 __str_6:
      007CD7 2D 46 32 35 36 2C 20  2245 	.ascii "-F256, "
      007CDE 00                    2246 	.db 0x00
      007CDF                       2247 __str_7:
      007CDF 4B 42 20 53 52 41 4D  2248 	.ascii "KB SRAM"
      007CE6 0A                    2249 	.db 0x0A
      007CE7 00                    2250 	.db 0x00
                                   2251 	.area XINIT   (CODE)
                                   2252 	.area CABS    (ABS,CODE)
