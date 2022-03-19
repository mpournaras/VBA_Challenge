# VBA_Challenge
This repository contains all the material for this stock analysis challenge 

## Overview of VBA_Challenge:

A client may want to look at stocks. Perhaps 5 of them, perhaps 500 of them! We are here to analyze a dataset of 12 tickers and determine the efficiencies and challenges gained or ecountered with different analysis styles. "Refactoring" code is defined as changing its internal structure without changing its external behavior. We will attempt to refactor some code and see if we can gain efficiencies.

## Results:

Here we have 2 sets of analysis. An analysis of stocks in 2017 and 2018 breaking down 12 tickers, aggregating total daily trade volumes, and measuring returns over time. The key here is we had 2 versions of code. 

Version 1 schema: The original "Tickers as a string" strategy. The 2017 stock analysis took .496 seconds, and a 2018 stock analysis took .484 seconds

![image](https://github.com/mpournaras/VBA_Challenge/blob/main/Resources/Stock_Analysis_2017.png)
![image](https://github.com/mpournaras/VBA_Challenge/blob/main/Resources/Stock_Analysis_2018.png)

Version 2 schema: The refactored "Indexed tickers" strategy. The 2017 stock analysis took .305 seconds, and a 2018 stock analysis took .285 seconds.

![image](https://github.com/mpournaras/VBA_Challenge/blob/main/Resources/VBA_Challenge_2017.png)
![image](https://github.com/mpournaras/VBA_Challenge/blob/main/Resources/VBA_Challenge_2018.png)

The "indexed ticker" schema was interesting in that the ticker was never named as a string until referencing it at the end to print the results. I believe it allowed for faster cycling through tickers and the results agree. Here is a display of the schema:

![image](https://github.com/mpournaras/VBA_Challenge/blob/main/Resources/Code_Example.png)

## Summary:

As the results clearly show, the refactored code is much faster. The refactored code is almost **40% faster** using the 2017 data and **almost 40%** faster with the 2018 data as well. 

There are 2 main benefits we can draw from this. 

"But Michael, how is saving .25 seconds significant?.. thats a blink of an eye!"

This was an analysis with 12 stock tickers. Lets say I wanted to do 120 tickers! Maybe over 2 years for each anaysis? That is 40x as much data. **These small efficiencies gained by refactoring this code would be magnified with larger data sets**

Another efficiency gained would be the portability of this code. When indexed we can absolutely plug in any number of tickers, any range of years, and quickly run the same analysis. **With small changes in this code we could sell this to many clients for many applications with minimal hours spent changing code.**

While I think the changes are great, there are some cons to be noted. it is slightly more complex to look at and understand. The original code was simple and made sense visually. But computers read things the same regardless of how easy it is for our human eyes. The hours spent refactoring will have numerous benefits down the road.
