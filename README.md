# Stooq-for-Finance-Quote
A [Finance::Quote](https://github.com/finance-quote/finance-quote) module (Perl), which retrieves financial data from [Stooq.com](https://stooq.com) website. It exposes asset's: name, price, open, high, low, close/last, ask, bid, volume and date/isodate/time of retrieval.

It is highly helpful with assets that are not present in other APIs like e.g. Polish mutual funds, bonds etc..

# Installation
Download file `Stooq.pm` and paste it into Finance::Quote directory (probably `<perl_dir>\site\lib\Finance\Quote`). Then add string `Stooq` (preferably in alphabetical order) to the `@MODULES` variable in `Quote.pm` (`<perl_dir>\site\lib\Finance`).

# Use
Method is called `stooq_stocks`.

# PLN only
Firstly, Stooq provides financial data for various assets but it never tells the asset's currency. (And I think it isn't likely to change soon, as I asked them). Secondly, the original author wrote this module because he needed to get financial data about Polish stock market. Due to this, the currency 'PLN' is hardcoded into the module and any request for financial data of a non-PLN asset will provide wrong information and may break your data.

If you need more flexibility, take a look at [StooqAPI-for-Finance-Quote](https://github.com/Kaligula0/StooqAPI-for-Finance-Quote).

# Unofficial
The module is unofficial. And it won't become official until Stooq adds the stock's currency to it's financial data in API response. You can read details in [Finance::Quote's bug #203](https://github.com/finance-quote/finance-quote/issues/203).

# Authors
The module isn't written by me – I only updated it, as it was outdated (in the moment of publication here it was almost a dozen years old). The file comes from [CPAN Bug Tracker – Bug #64474 for Finance-Quote: New module suggestion for Warsaw Stock Exchange (stooq.com)](https://rt.cpan.org/Public/Bug/Display.html?id=64474), and the original author is Michał Fita.

# License
GPL 2.0 as original.
