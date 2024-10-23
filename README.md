# CMC-watchlist-click




<th class="stickyTop" style="text-align: end;"><div class="sc-31e84ac2-0 HETIK sortable-header-container"><div class="sc-31e84ac2-1 cDNchY"><span class="sc-31e84ac2-2 hZReMd icon-wrapper"><span class="icon-Caret-down"></span></span><p class="sc-71024e3e-0 llNEXf" font-size="0" color="text" data-sensors-click="true">1h %</p></div></div></th> 

在 tampermonkey 中，仅在 网站 coinmarketcap.com 中，对 sc-71024e3e-0 llNEXf 进行点击操作。每次点击间隔 9秒。

// ==UserScript==
// @name         CoinMarketCap Clicker
// @namespace    http://tampermonkey.net/
// @version      1.0
// @description  Click specific elements on coinmarketcap.com.
// @match        *://*.coinmarketcap.com/*
// @grant        none
// ==/UserScript==

(function () {
    'use strict';

    function clickElements() {
        const elements = document.querySelectorAll('p.sc-71024e3e-0.llNEXf');
        if (elements.length > 0) {
            elements.forEach(element => {
                element.click();
            });
        } else {
            console.warn('[-] No elements found to click.');
        }
    }

    setInterval(clickElements, 9000);
})();


 
