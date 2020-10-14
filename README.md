# Eve Echoes Reprocessing Database

The [reprocessing.csv](https://github.com/eve-echoes-db/reprocessing/blob/main/reprocessing.csv) file contains reprocessing amounts for items in Eve Echoes.

All the amounts are based on 100% reprocessing efficiency. To get the amounts based on your character, multiply the values by your character's reprocessing effeciency skill. All skills start out at 30% with a new character. Skilling various Resource Processing values will improve that percentage.

## How do I read this data?

There are four columns: Skill, Item, Component and Amount.

-   The Skill column refers to the Skill you can Improve in the game to increase the amount of Components you get for reprocessing the Item.
-   The Item column is the object in the game that you reprocess and get the Components from. ie: the input column.
-   The Component column refers to the Components you get after reprocessing an Item. ie: the output column.
-   The Amount column refers to the amount you'll get from reprocessing an Item.

A single Item can be on multiple rows. Each row corresponds to a different output Component. For example, Veldspar only has one row because you only get Tritanium from processing Veldspar. Pyroxeres has four rows, because it has four Components after reprocessing (Tritanium, Pyerite, Mexallon, Isogen).

## Importing into Google Sheets

-   Create a new Sheet
-   Copy and paste the below text into a cell:

```
=importdata("https://raw.githubusercontent.com/eve-echoes-db/reprocessing/test/reprocessing.csv")
```

-   After a couple of seconds the table should show up in your Sheet.

## FAQs

> The ore amounts are 100 times bigger in the game. What's going on?

Ore reprocessing amounts in the Reprocessing Database are based on a single ore, not the 100 minimum you need to reprocess.

## Contributing

The Reprocessing Database may be missing items or have out of date amounts. If you notice something please do one of the following:

-   Fill out the [feedback form](https://docs.google.com/forms/d/e/1FAIpQLScrNLp-kQfasp6gOz9FSD-CvBn-FMdMl2RJpGockumAJodYpQ/viewform).
-   Submit a Pull Request.
