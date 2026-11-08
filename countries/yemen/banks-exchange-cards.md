> **Source:** `sharrwah-knowledge-map@caad5aa1a052b74b05e34ea0edb3b3336727c149:yemen-setup-options/notes/banks_exchange_cards.md`  
> **Written:** 9 October 2026 (research date stated in the original; committed 10 October 2026). Earlier research, not reviewed since; re-verify before use.  
> **Excerpt:** the title, the reading notes and Q1–Q5 (Takeaway, Cited Findings and Gaps), copied verbatim. Omitted: every "Inferences" subsection, the scope paragraph, Q5's Takeaway, and 9 further passages: the reading note about the omitted Inferences, five passages on what a platform could do, two items naming individual developers' code packages, and one item sourced from a reference platform's forum.

---

# Yemen non-wallet payment rails for online commerce: banks, money-exchange and remittance networks, cards, foreign processors, crypto

How to read these notes:
- Every line under "Cited Findings" has a source. Where I could not read the primary page (PDF dumps, 403s), the line says it came from a search-result summary and should be treated as weaker.
- Background that applies to every rail: Yemen has two central banks, CBY-Aden (internationally recognized) and CBY-Sana'a (Houthi). It also has two rial note series with very different values: "old" notes in the Houthi north, roughly YER 530–540/USD in 2024–25, and "new" notes in the government south, roughly YER 1,800–1,900/USD in 2024 and up to YER 3,000/USD in 2025. In addition, SAR and USD circulate widely. Because of this split, the currency and the territory together define every rail.

---

## Q1. How do Yemeni banks support payments today? (accounts, transfers, mobile apps, APIs/corporate integration, virtual accounts or payment references, which banks are large and where they operate)

### Takeaway
Banks reach only a small minority of Yemenis: about 4.8% of adults hold deposits, and account ownership of any kind, wallets included, is about 9%. There is still no interbank instant-payment system. CBY-Aden approved a fast payment system (FPS) operator company and a mandatory national QR standard in March 2026, but these are not yet live. In practice, "bank payment" today means one of two things:
- an intra-bank transfer inside one large bank's app, mostly Al-Kuraimi (KJ / Mfloos), Tadhamon and a few others;
- a bank-run merchant API. Kuraimi's "E-Payment" API, in which a buyer approves a payment from the Kuraimi app, is the clearest example of a payment-reference integration a platform could plug into.

The 2024–2025 sanctions shocks were the OFAC designations of Yemen Kuwait Bank (YKB) and International Bank of Yemen (IBY), the March 2025 US designation of the Houthis as a Foreign Terrorist Organization (FTO), and the forced relocation of bank headquarters to Aden. Together they make a bank's reliability depend on which authority it answers to.

### Cited Findings

**Scale of banking / inclusion**
- "The population is almost entirely unbanked, including about 90% of men and 99% of women. Just 1.6 percent of adults borrow from formal financial institutions, while 4.8 percent have deposits... Only 6.3 percent of adults have access to financial service points, and there are just 1.6 bank branches per 100,000 adults." Formal banking is "largely restricted to major cities, while rural and remote areas are mainly served by money exchangers." — [World Bank, Yemen Financial Sector Diagnostic (Dec 2024)](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- Findex account ownership rose from 3.7% (2011) to 6.4% (2014). A 2022 study (SMEPS, 2023) found that about 8.8% of the population owned an account of any type, including e-wallets. The World Bank says inclusion "likely worsened during the conflict." — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- In 2014, 94% of adults had no financial account. By 2019, 3 million Yemenis (10% of the population) held at least one account, 27% of them e-money accounts. Only 2% of women held an account. Between 2015 and 2016 the number of open accounts fell 40%, to about 2.4 million accounts held by 1.5 million people. — [Sana'a Center, "Challenges and Prospects for Electronic Money and Payment Systems in Yemen" (Mar 2022)](https://sanaacenter.org/files/Rethinking_Yemens_Economy_No10_En.pdf)
- Firms: in 2022, 59% of formal firms used exchange companies as their main financial intermediary and only 20% used commercial banks. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)

**Which banks exist and which are large**
- The CBY-Aden list reproduced by the World Bank names 29 banks:
  - State-owned commercial banks: Yemen Bank for Reconstruction and Development, National Bank of Yemen (NBY), CAC Bank.
  - Private commercial banks: Yemen Kuwait Bank, (Yemen) International Bank, Yemen Commercial Bank, Yemen Gulf Bank, Hadramout Commercial Bank (2022), First Aden Islamic Bank (2024).
  - Islamic banks: Tadhamon, Saba Islamic, Yemeni Islamic Bank, Shamil Bank of Yemen & Bahrain (SBYB), Al-Kuraimi Islamic Bank.
  - Foreign banks: UBL, Arab Bank, Rafidain, QNB.
  - Microfinance banks: Al-Amal, Al-Kuraimi Islamic Microfinance, Al-Qutaibi, Aden MF, Al-Busairi, Alinma MF, **Bin Dowal Islamic Microfinance (2022)**, Shamoul, Sharq Yemen, Al-Qasemi, Tamkeen. — [World Bank FSD 2024, Table 2](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- The World Bank's stress test used "seven of the ten largest commercial banks": IBY, Tadhamon, CAC, NBY, Kuraimi Islamic Microfinance Bank, YKB and Yemen Commercial Bank. It names IBY, CAC and NBY among "the country's largest banks." Tadhamon "remains one of Yemen's largest banks" (37 branches, largest shareholder the Hayel Saeed Anam Group). Al-Kuraimi is the second-largest microfinance institution. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- Some large money exchangers have turned into banks. Al-Kuraimi and Al-Qutaibi became microfinance Islamic banks, and Bin Dowal was finalizing a microfinance bank licence. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)

**Interbank infrastructure / instant payments**
- CBY-Aden payment-systems work since 2019 has included a payment systems department and "SWIFT activation for near-same-day settlements." An automated clearing house (ACH) and a real-time clearing system (RTCS) were still "proposals... pending financing" (as of the 2024 report). Yemen joined the Arab Monetary Fund's Buna cross-border platform. Three Aden commercial banks offered e-wallets as of Dec 2023. — [World Bank FSD 2024, Box 11](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- By Dec 2023, most banks in Sana'a and Aden were connected to Swiftscope, which lets the central bank monitor banks' transactions. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- On 10 July 2025, CBY-Aden met all banks to discuss setting up an instant-payment company ("شركة الدفع الفوري") with "direct World Bank support." The same meeting discussed restructuring the Unified Network company, raising its capital and handing its management "fully to the banking sector." — [Belqees, 10 Jul 2025](https://belqees.net/locals/%D8%A7%D9%84%D9%85%D8%B1%D9%83%D8%B2%D9%8A-%D9%81%D9%8A-%D8%B9%D8%AF%D9%86-%D9%8A%D8%AC%D8%AA%D9%85%D8%B9-%D8%A8%D9%85%D9%85%D8%AB%D9%84%D9%8A-%D8%A7%D9%84%D8%A8%D9%86%D9%88%D9%83-%D8%A7%D9%84%D9%8A%D9%85%D9%86%D9%8A%D8%A9-%D9%84%D8%A8%D8%AD%D8%AB-%D8%AA%D8%A7%D8%B3%D9%8A%D8%B3-%D8%B4%D8%B1%D9%83%D8%A9-%D8%A7%D9%84%D8%AF%D9%81%D8%B9-%D8%A7%D9%84%D9%81%D9%88%D8%B1%D9%8A-%D9%88%D8%A7%D8%B9%D8%A7%D8%AF%D8%A9-%D9%87%D9%8A%D9%83%D9%84%D8%A9-%D8%A7%D9%84%D8%B4%D8%A8%D9%83%D8%A9-%D8%A7%D9%84%D9%85%D9%88%D8%AD%D8%AF%D8%A9)
- On 29 March 2026, the CBY-Aden board made three decisions:
  - the central bank becomes "a principal shareholder in the Fast Payment System (FPS) operator company";
  - "a unified, binding national standard for QR Code service for all financial institutions" was adopted;
  - linking of e-wallets through unified connection routes was approved.

  No go-live date was given. — [CBY-Aden news/922 (29 Mar 2026)](https://cby-ye.com/news/922)
- A national switch has existed on paper since before the war. The CBY supported 11 banks in founding the Yemen Financial Services Company (YFSC) to run a "National Financial Switch Interbank Network," and a 2014 CBY circular endorsed a bank-led e-money model. This comes from a search-result summary of the paper; I read the table of contents, which confirms a section "4.3 The National Financial Switch Interbank Network," but not the section text. — [Sana'a Center (Mar 2022)](https://sanaacenter.org/files/Rethinking_Yemens_Economy_No10_En.pdf)

**Bank apps and merchant APIs (payment references)**
- An app-store aggregator lists a new Alkuraimi Islamic Bank app (first released 11 Aug 2025) offering "instant money transfers" and real-time statements. This came from a search summary of an aggregator listing (weak). — [mwm.ai listing](https://mwm.ai/apps/ki-bank-app/6748606298)
- Bank-led e-money licences (CBY, 2015–2019) went to Al-Kuraimi Islamic Microfinance Bank, Tadhamon, Al-Amal Microfinance Bank and YKB. CBY-Sana'a licensed CAC Bank, and in Jan 2021 also SBYB and IBY. — [Sana'a Center (Mar 2022)](https://sanaacenter.org/files/Rethinking_Yemens_Economy_No10_En.pdf)
- A Yemeni e-commerce blog names Floosak, founded in 2016 by "Yemen Kuwait Bank," which works by mobile number without a bank account, and a "Pyes" service from Al-Amal Microfinance Bank. This is a search snippet of a commercial blog (weak). — [Fatora blog](https://fatora.io/blog/online-payment-in-yemen/)

**Sanctions, relocation and split-authority disruptions (bank reliability)**
- April 2024: CBY-Aden ordered all banks to move their headquarters from Sana'a to Aden within 60 days (Decision 17 of 2024). — [SEMC policy paper (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- On 3 July 2024, CBY-Aden revoked the licences of six Sana'a-headquartered banks: Tadhamon, YKB, SBYB, Al-Amal Microfinance, Al-Kuraimi Islamic Microfinance and IBY. The Houthi Money Changers Syndicate suspended dealings with CBY-Aden-controlled exchange networks. — [Sana'a Center, Yemen Review Jul–Sep 2024](https://sanaacenter.org/the-yemen-review/july-sept-2024/23500)
- On 23 July 2024, a UN-announced, Saudi-brokered deal had both sides cancel "all the recent decisions and procedures against banks... and refrain[] in the future from any similar decisions." The Houthis had banned dealings with 13 Aden banks in retaliation. — [Gulf News, 23 Jul 2024](https://gulfnews.com/world/gulf/yemen/al-houthis-yemen-govt-reach-financial-de-escalation-deal-un-envoy-1.103583412); [The New Arab](https://www.newarab.com/news/houthis-yemeni-government-reach-financial-de-escalation-deal)
- On 17 Jan 2025, OFAC designated Yemen Kuwait Bank for supporting the Houthis, with a wind-down general licence to 16 Feb 2025. — [Willkie Compliance Concourse](https://complianceconcourse.willkie.com/articles/united-states-sanctions-yemen-kuwait-bank-for-supporting-the-houthis/); [Treasury release via GlobalSecurity](https://www.globalsecurity.org/military/library/news/2025/01/mil-250117-treasury02.htm)
- On 17 Apr 2025, OFAC designated the International Bank of Yemen (Sana'a) and three senior officials for giving the Houthis SWIFT access and other support. — [US Treasury sb0092](https://home.treasury.gov/news/press-releases/sb0092)
- On 4 Mar 2025, the US designated the Houthis a Foreign Terrorist Organization, and Sana'a banks began moving their headquarters to Aden. — [Barran Press, 14 Mar 2025](https://en.barran.press/news/6377); [Xinhua, 15 Mar 2025](https://english.news.cn/20250315/312bd698021244cc9ec3e80617c17f35/c.html)
- Eight banks notified CBY-Aden of relocation, including Tadhamon, Yemen Commercial Bank and Saba Islamic Bank. — [South24](https://south24.net/news/newse.php?nid=4542)
- By late 2025, "all major banks and leading exchange companies" had moved their headquarters to Aden, "making the Yemeni banking sector fully operational from Aden, according to the Governor of Aden-CBY." — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- Correspondent banks follow CBY-Aden directives and "requested proof of relocation" from institutions wanting to keep international transactions. — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- Earlier deposit freezes: CBY-Aden and CBY-Sana'a set conflicting withdrawal rules (CBY-Sana'a allowed withdrawals only on deposits accumulated since 2017), which "de facto froze most cash deposits made before" the split. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)

### Gaps
- No official Kuraimi E-Pay documentation, fees, limits, settlement terms or onboarding criteria found. kuraimibank.com did not surface in search. The same goes for Tadhamon, SBYB (Shamil Money), CAC, YKB and Al-Amal merchant APIs.
- No source on whether any bank offers virtual accounts, payment references, corporate host-to-host or statement APIs.
- No current (2025–26) customer/account totals per bank. No ranking of banks by assets beyond the World Bank's qualitative "largest" list.
- The status of YFSC / the national switch after 2015 is unknown. MEPS Yemen mentions ATM and POS management but no switch (see Q3). The relationship between the planned FPS company and the existing switch is unclear.
- How Sana'a-area branches of relocated banks operate in 2026 (accounts, transfers in old rials) was not found. The Barran (Mar 2025) article does not say.
- No Global Findex 2025 figure for Yemen found. Yemen appears to be absent from recent Findex rounds; the latest is 2014.

---

## Q2. How do exchange companies and remittance networks work for domestic payments, what do they cost, and could a platform use them to collect from buyers or pay sellers?

### Takeaway
Exchange companies, not banks, are Yemen's real domestic payment network. They hold most cash outside banks, serve far more people than banks do, and are the main intermediary for most firms. Since June 2024, CBY-Aden has required that all domestic cash transfers by exchange companies run through a single network, the Unified Money Network (UNMONEY / الشبكة الموحدة للأموال). It says the network consolidated 22 previous transfer networks, carried more than YER 251 billion in 2024, and now includes all banks and e-wallets. UNMONEY was restructured in July 2026 so that banks are shareholders.

### Cited Findings

**Size and role**
- Money exchangers are "the primary destination for deposits and the main source of credit for traders," "serve a much larger share of the population than Yemeni banks," and "operate more extensive networks than banks." They hold 12–15% of banking-sector assets but 35–40% of its net foreign assets. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- 71% of communities rely on informal exchange outlets, and 64% use hawala as their primary way to transfer money rather than banks (citing the World Bank). — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- Counts of exchange businesses (citing the World Bank FSD):
  - By 2023, Aden had 332 licensed individual exchange outlets, 96 exchange companies and 86 money-transfer agents, and Sana'a had more than 170 licensed exchange companies.
  - Between 2014 and 2023, exchange companies grew from 179 to 415 in Sana'a and from 34 to 91 in Aden.
  - In 2018, about 800 of 1,350 outlets operated without a licence.

  — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- Legal limits: Law No. 19 of 1995 (Arts. 21–23) "prohibit exchange companies from performing banking functions such as commercial financial transfers, opening accounts, conducting credit and debit operations." The parallel market has nevertheless "surpassed them." — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- CBY-Aden prohibits non-bank institutions from accepting deposits and has pushed large exchangers either to obtain banking licences or to return deposits. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- CBY-Aden capital minimums (Decision 58 of 2022): YER 1 bn for exchange companies, YER 500 m for individual outlets, YER 100 m for remittance agents. — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)

**Named networks**
- "Most exchange companies engage in interregional transactions facilitated by remittance networks such as the Al-Najm and Al-Imtiaz networks." About 22 exchangers launched a joint network with CBY-Aden support to restore interoperability. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- Emtiaz Express is owned by Al-Montab Exchange, one of the 25 largest exchange companies, with assets of about YER 13.7 bn. A leaked 2023 list showed 1,927 unclaimed transfers, 60% of their value in YER, which "indicat[es] that most of the transfers were domestic." Networks then built name-search tools for unclaimed transfers, and CBY-Aden required reporting of unclaimed transfers after two months. — [World Bank FSD 2024, Box 7](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- One network reportedly held more than 60,000 uncollected transfers, worth nearly YER 2 bn and more than SAR 6 m (Al Jazeera, Feb 2023). — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- Al-Kuraimi and Al-Qutaibi are former exchangers that are now microfinance banks. Bin Dowal was converting into Bin Dowal Islamic Microfinance Bank, listed in 2022. Al-Amal is a microfinance bank (2008), not an exchange company. — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)

**Unified Money Network (UNMONEY)**
- Origin: CBY-Aden Decree No. 18 of 2020 (Nov 2020 resolution). UNMONEY was officially activated in Feb 2024 with initial capital of YER 5 bn. Capital was later raised to YER 12 bn as relocated banks joined (CBY statement, July 2025). — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf); [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- Decision No. 23 of 2024 (26 June 2024) did the following:
  - It halted "completely and permanently" the domestic transfer networks owned by banks and exchange companies.
  - It required new domestic cash transfers to go "through the unified network (UNMONEY)" and banned other domestic cash transfers.
  - Bank networks could run in parallel until 30 July 2024.
  - E-wallets and licensed PSPs were exempt within set caps.
  - Pending items had to be liquidated within 15 days and undelivered transfers reported within 20 days.
  - Penalties include licence withdrawal and fines.

  — [CBY-Aden news/706](https://cby-ye.com/news/706)
- Same day: CBY-Aden circular banning banks and exchanges from dealing with 12 unlicensed entities, wallets and e-payment services. — [CBY-Aden news/703](https://cby-ye.com/news/703)
- The Houthi response: CBY-Sana'a condemned the decree, and the Houthi Money Changers Syndicate suspended dealings with CBY-Aden-controlled exchange networks. — [Sana'a Center Yemen Review Jul–Sep 2024](https://sanaacenter.org/the-yemen-review/july-sept-2024/23500)
- A Barran Press article says the Houthis "restricted dealings with the unified network and required two currencies of differing sizes and values, which increased domestic transfer fees." The same article says there are "thousands" of transfer networks, mostly outside central-bank control. — [Barran Press (June 2024)](https://en.barran.press/news/3195)
- At the CBY-sponsored cashless expo in Aden on 22 Jan 2026, CBY said it had consolidated 22 cash transfer networks into one unified network, that more than YER 251 bn was transacted through it in 2024, and that "all banks and e-wallets have joined the network." — [CBY-Aden news/915 (22 Jan 2026)](https://cby-ye.com/news/915)
- On 27 July 2026, an extraordinary general assembly of the Unified Money Network Company approved a completed capital increase, a shareholder base widened to "the banks operating in Yemen," and a new nine-member board. CBY calls the company "a key pillar for developing the payments system." — [CBY-Aden news/957 (27 Jul 2026)](https://cby-ye.com/news/957)
- Feb 2025 measures reported in a search summary: CBY-Aden circulars halted FX buying and selling through digital platforms and apps, and required exchange companies to clear pending balances with UNMoney "or similar networks" within two weeks. I did not open the page, so this is a snippet. — [South24](https://south24.net/news/newse.php?nid=4503)
- 2024–2026 enforcement: there were repeated licence suspensions and closures of exchange companies and agents:
  - 11 companies in July 2024 ([Sana'a Center](https://sanaacenter.org/the-yemen-review/july-sept-2024/23500));
  - Governor's Decisions Nos. 14, 15, 17 and 18 (2026), listed on the CBY site ([CBY-Aden news/922 page listing](https://cby-ye.com/news/922));
  - "Suspends Licenses of 12... Bringing Total to 15" (search snippet only) ([Barran](https://en.barran.press/news/3291)).

**International remittance channel rules (relevant to diaspora → Yemen)**
- On 28 May 2024, CBY-Aden limited the receipt of international transfers to banks and exchange companies it has qualified, operating through Aden head offices and their branches. Sub-agents may serve under annual contracts. Remittances must be paid in the currency sent unless the beneficiary chooses otherwise. — [Asharq Al-Awsat, 28 May 2024](https://aawsat.com/node/5025163)

**Costs**
- No published domestic fee schedule for UNMONEY or any exchange company was found. Barran says fees rose because of the dual currency, without figures ([Barran](https://en.barran.press/news/3195)). Global transfer companies and hawala agents are said to have "relatively low fees and extensive networks" ([World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)).

### Gaps
- No fee table for UNMONEY, Al-Najm, Al-Imtiaz/Emtiaz, Bin Dowal or Kuraimi domestic transfers (YER or %), and no per-transfer or daily limits.
- Whether UNMONEY exposes an API or reference-lookup service to third parties (merchants or platforms) is unknown, as is whether bank and wallet members can deliver into accounts or wallets rather than cash.
- Cancellation and refund rules for unpaid transfers are unknown.
- Whether the Houthi side ran its own parallel unified network in 2025–26, and the current state of north-south transfers after the 2025 relocations and FTO designation, were not found.
- Many of the 2025–26 licence-suspension articles name companies only in attached PDFs that I did not read.

---

## Q3. Is card acquiring for e-commerce available in Yemen (online gateway, 3-D Secure, local switch)? What share of people hold cards?

### Takeaway
Card ownership is tiny: about 400,000 active debit cards at end-2019 (mostly used at ATMs) and about 1,200 active credit cards, in a population above 30 million. POS terminals numbered only 817 in 2019. There is at least one live, CBY-licensed e-commerce card gateway: MEPS Yemen (the National Payment Company). It accepts local and international Visa, Mastercard, Amex and UnionPay cards via Mastercard Payment Gateway Services (MPGS), Visa CyberSource and PayTabs, and it offers payment links and invoicing. Some banks issue online-capable cards: CAC's Visa "Net" card (internet only) and SBYB's "WebSurfer" prepaid Mastercard. For domestic buyers, cards are a niche rail. They matter mainly for diaspora and foreign-card buyers.

### Cited Findings
- Active debit cards fell from more than 1 million (2014–15) to 200,000 by end-2016, then recovered to about 400,000 at end-2019, "mostly used for ATM services." Active credit cards fell from about 6,600 (2014) to 1,206 (2019). — [Sana'a Center (Mar 2022)](https://sanaacenter.org/files/Rethinking_Yemens_Economy_No10_En.pdf)
- ATMs: 6.4 per 100,000 adults in 2014. POS fell to 200 devices in 2016 from 1,500 in 2014, then "tripl[ed] to reach 817 in 2019." — [World Bank FSD 2024](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- MEPS Yemen (الشركة الوطنية للمدفوعات) "electronic payment gateway":
  - It accepts local and international cards (Mastercard, Visa, American Express, UnionPay).
  - It is powered by Mastercard Payment Gateway Service (MPGS), Visa CyberSource and PayTabs (KSA).
  - It offers on-site checkout without redirect, plugins, e-invoicing by email or SMS with payment URL, and fixed-amount payment links for social media.
  - It says it is licensed by the Central Bank of Yemen and was formed by Middle East Payment Services (MEPS) and the National Cash Transfer Company.
  - Other services: ATM management, POS operation, card issuance and e-collection.
  - 3-D Secure, currencies, fees and settlement are not stated.

  — [MEPS Yemen, Electronic Payment Gateway page](https://www.mepsyemen.com/electronic-payment-gateway); [MEPS Yemen home](https://www.mepsyemen.com/)
- MEPS took part in the CBY-sponsored cashless expo in Aden (22 Jan 2026), alongside more than 9 e-wallets and the unified network. — [CBY-Aden news/915](https://cby-ye.com/news/915)
- CAC Bank "Visa Net" card is used "to buy from internet only." It cannot be used at POS or ATMs. CAC's other Visa cards work at ATMs, POS and online. — [CAC Bank Visa Cards page](https://www.cacbank.com.ye/en-Us/Contents/SubPage/Visa-Cards)
- SBYB "WebSurfer" is a prepaid Mastercard for online shopping, "accepted on most websites worldwide," and recharged via the Shamil Money app. Undated bank marketing page. — [SBYB Electronic Cards Service](https://www.sbyb.net/en/service/17)
- National Bank of Yemen issues Silver and Gold Visa and Mastercard credit cards with Arab Financial Services (Bahrain). Undated. — [NBY credit cards](http://www.nbyemen.com/creditCard_en.html)
- SabaCard was founded in 2005 by Al Rowaishan Group and Yemen Commercial Bank. It describes itself as "the first local e-payment solutions provider" and offers ATM and POS switching, working with Mastercard and Visa. — [SabaCard](https://www.sabacards-rg.com/en/)
- UnionPay International signed with CAC Bank to issue UnionPay cards in Yemen. The URL slug suggests 29 Dec 2014. — [Electronic Payments International](https://www.electronicpaymentsinternational.com/news/unionpay-partners-with-cac-to-issue-payment-cards-in-yemen-291214-4478310)
- A third-party payouts firm lists Al-Kuraimi Bank Mastercard BINs as having a "history of successful transactions" (weak, operational evidence only). — [Mellow help center](https://help.mellow.io/en/articles/9647437-tested-bank-cards-of-yemen)
- CBY-Aden adopted a mandatory national QR standard (29 Mar 2026). This is a non-card alternative for in-person and online "scan to pay." — [CBY-Aden news/922](https://cby-ye.com/news/922)

### Gaps
- No MEPS Yemen pricing, settlement time, currency list, 3-D Secure confirmation, acquiring bank, or merchant onboarding criteria. No count of live merchants.
- No 2020–2026 data on card numbers, POS counts or online card usage. No Global Findex card-ownership figure for Yemen after 2014.
- No current Visa or Mastercard country pages or press releases for Yemen found. Whether Saudi mada cards can be accepted via MEPS Yemen is unknown.
- Whether any other Yemeni bank (Tadhamon, Kuraimi, YCB, CAC) operates its own e-commerce acquiring gateway was not established.

---

## Q4. Which foreign payment processors or wallets accept Yemeni merchants or Yemen-based buyers, and which explicitly exclude Yemen? How do diaspora buyers pay for goods delivered in Yemen today?

### Takeaway
None of the mainstream global processors onboard Yemen-based merchants:
- Stripe does not list Yemen.
- Wise explicitly does not support Yemen.
- PayTabs' published coverage (per an integrator) excludes Yemen, although MEPS Yemen uses PayTabs behind its own gateway.
- PayPal's Yemen status is unconfirmed, at best "send-only."
- Several fintechs (Rho, CoinGate, Wallex) list Yemen as restricted.

Diaspora money reaches Yemen mainly through three channels:
- Yemeni banks: USD 4.9 bn inbound in 2022.
- Western Union and MoneyGram: USD 1.1 bn inbound in 2022.
- Yemeni exchange-company agents abroad, especially in Saudi Arabia, in a hawala pattern.

### Cited Findings

**Exclusions / availability**
- Stripe "Global availability" lists 51 countries. Yemen is not listed. The UAE is the only nearby Middle East country listed; Saudi Arabia is not. — [Stripe Global](https://stripe.com/global)
- Wise lists Yemen under "Countries and regions we don't support." Users there cannot register, and Wise cannot "send or receive money to or from" these places. — [Wise Help: countries we can send to](https://wise.com/help/articles/2978049/what-countries-and-regions-can-i-send-money-to)
- PayPal has a Yemen-locale page (/ye/) offering send and pay functions. PayPal says members in some countries "may only use PayPal to send payments and not receive payments." No Yemen-specific statement was found. A Wise hub page claims PayPal is "accepted in Yemen" (secondary source). — [PayPal /ye/](https://www.paypal.com/ye/webapps/mpp/home); [PayPal Help: send-only](https://www.paypal.com/va/cshelp/article/why-does-my-paypal-account-have-only-send-capabilities-help1027); [Wise payment-methods hub (Yemen)](https://wise.com/gb/hub/payment-methods/yemen)
- PayTabs coverage per an integrator: UAE, Saudi Arabia, Egypt, Oman, Jordan, Kuwait, Iraq. Yemen is not listed. Integrator page, not PayTabs' own. — [Mewayz PayTabs docs](https://mewayz.com/docs/payment-gateway-paytabs). Separately, MEPS Yemen lists PayTabs among its back-end processors ([MEPS Yemen](https://www.mepsyemen.com/electronic-payment-gateway)).
- Rho lists Yemen as restricted. CoinGate lists it among jurisdictions where payments are not permitted. Wallex cannot send to or receive from Yemen. These are search summaries. — [Rho](https://www.rho.co/hc/restricted-countries-and-international-payment-types); [CoinGate](https://support.coingate.com/hc/en-us/articles/23236010880412-Countries-and-territories-not-supported-for-payments); [Wallex](https://help.wallex.asia/list-of-restricted-countries)
- Payoneer's prohibited-transactions page says eligibility depends on "country of residency or incorporation," but the search summary showed no Yemen-specific statement. — [Payoneer prohibited list](https://www.payoneer.com/ar/legal/prohibited-transaction-list/)

**How diaspora money flows today**
- In 2022, Yemen's banking sector processed USD 4.9 bn inbound and USD 5.6 bn outbound transfers. Most inbound transfers were in USD, then SAR, EUR and AED. Western Union and MoneyGram are "the second largest channel," with USD 1.1 bn inbound in 2022 (USD 400 m in Q1 2023) and a net inflow of USD 945 m. — [World Bank FSD 2024, Box 8](https://documents1.worldbank.org/curated/en/099102324070011985/pdf/P177631-d18a7ee4-3fcf-4393-9665-77f98b3e43a7.pdf)
- Typical hawala flow from Saudi Arabia: an expatriate pays a Yemeni exchange company's agent in KSA, and the Yemeni exchange pays the beneficiary in Yemen "at the parallel-market exchange rate." The agent then uses the KSA balance to pay importers' suppliers abroad. "Electronic banking services in neighboring countries have facilitated these operations." — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- A large share of remittances bypasses banks and goes through exchange companies or informal networks (ACAPS, Oct 2021). — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- Remittances are about 20% of GDP (2023), per a search summary of the IGC brief. The same brief puts 2025 exchange rates at about 530 YER/USD in Houthi areas and 1,550 in government areas. — [IGC, "From Cash to Capital" (Feb 2026)](https://www.theigc.org/sites/default/files/2026-02/From-Cash-to-Capital-Leveraging-Remittances-for-Yemens-Economic-Future.pdf)
- Formal inflows are estimated at USD 4–6 bn, and informal flows possibly up to USD 10 bn. International bank de-risking has narrowed formal options. Search summary. — [AidData](https://www.aiddata.org/blog/leveraging-remittances-for-economic-recovery-in-yemen)
- STC Pay (KSA) international transfers can be collected at Western Union locations ("more than 525,000 worldwide") or sent to bank accounts or wallets. The World Bank Remittance Prices database lists an STC Pay Saudi→Yemen entry (data collected 6–15 Nov 2024). I could not open the RPW page (403); this is a search summary. — [STC Pay international transfer](https://stcpay.com.sa/international-transfer); [World Bank RPW SA→YE](https://remittanceprices.worldbank.org/corridor/SA/YE)
- Since 28 May 2024, only CBY-Aden-qualified banks and exchange companies, and their sub-agents, may pay out international remittances. Payout must be in the currency sent. — [Asharq Al-Awsat](https://aawsat.com/node/5025163)
- In the Saudi→Yemen hawala, the exchanger profits from FX margins: for example it sells USD at SAR 3.85 versus the official 3.75. — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- About 3 million Yemenis work in Saudi Arabia (search summary of a Noonpost article; undated and weak). — [Noonpost](https://www.noonpost.com/41375/amp/)

### Gaps
- Official PayPal country terms for Yemen (full vs send-only vs unavailable) not confirmed. Payoneer's Yemen status not confirmed. Checkout.com, HyperPay, Moyasar and Tap coverage not individually checked. I found nothing showing they onboard Yemeni entities, and PayTabs (per an integrator) does not.
- No source on whether Saudi wallets (STC Pay, urpay) or banks (Al Rajhi's Tahweel, Enjaz) pay directly into Yemeni bank accounts or wallets (e.g., Kuraimi) rather than WU cash. No RPW cost figures (403).
- No evidence found of Saudi- or US-based e-commerce sites that sell goods for delivery inside Yemen and how they collect. The only result was a corporate gifting site (Giftsenda) with marketing claims. This "diaspora gift-commerce" practice remains unverified.
- No processor statements on whether they would accept a non-Yemeni merchant entity whose sellers or deliveries are in Yemen.

---

## Q5. Is crypto or USDT used in practice for commerce or remittances in Yemen?

### Cited Findings
- OFAC added eight Tron wallet addresses linked to a Houthi financial-facilitator network (Sa'id al-Jamal) to the SDN list. The addresses "largely transacted with Tether's USDT," and coverage says they reportedly moved nearly USD 1 bn (a secondary figure). The action is from 2025 per coverage; the exact date was not verified. — [Decrypt](https://decrypt.co/312999/us-treasury-sanctions-tron-wallets-tehter-houthis); [TRM Labs](https://www.trmlabs.com/post/us-treasury-sanctions-houthi-financial-networks-including-eight-crypto-addresses)
- TRM links the funds to IRGC-QF and al-Jamal entities such as Davos Exchange and Remittances Company, which operated "under the guise of legitimate financial institutions." It also notes Houthi crypto-mining since at least 2017 with limited impact. — [TRM Labs](https://www.trmlabs.com/post/us-treasury-sanctions-houthi-financial-networks-including-eight-crypto-addresses)
- Dec 2023: OFAC targeted the head of the Sana'a Currency Exchangers Association and exchange houses moving funds for al-Jamal. — [US Treasury jy2014](https://home.treasury.gov/news/press-releases/jy2014)
- SEMC lists "Cryptocurrency trading to obscure the origin of funds" among the parallel market's money-laundering methods. — [SEMC (Dec 2025)](https://economicmedia.net/en/wp-content/uploads/2025/12/The-Parallel-Market-in-Yemen-Banking-Sector-December-2025.pdf)
- The AGSI (Feb 2020) piece on the Yemeni "e-rial" describes a CBY-Sana'a digital balance (in trial since 2018) usable for a few services such as phone, water and electricity bills. It is not cryptocurrency. — [AGSI](https://agsi.org/ar/?p=22899)
- A NewHedge guide says Binance advertised YER P2P support, and that users worry about account freezes for Yemen residents. This is a promotional, unverified source. — [NewHedge](https://newhedge.io/buy/yemen)
- Arabic-language sites sell USDT, Perfect Money and Payeer balances to Yemenis (e.g., "المتجر اليمني للدفع الإلكتروني"). These are commercial listings with no usage data. — [ysfep.com](https://www.ysfep.com/); [Digibankar guide](https://digibankar.com/docs/transfer/yemen/global/)

### Gaps
- No survey data on crypto ownership or P2P volumes in Yemen. No explicit CBY-Aden or CBY-Sana'a statement on cryptocurrency found in this session.
- Exact date and Treasury press-release number for the Tron-wallet designation not verified.
