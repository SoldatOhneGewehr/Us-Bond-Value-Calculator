# Us-Bond-Value-Calculator
This python code calculates a bonds market value throughout its lifetime and graphs it.

## Purpose of This Project
This code helps user to see the market value of any US treasury bonds market value throught of its lifetime. Although bonds will return their face value as they expire, when the bondholder wants to sell his/her bond, the market value most likely will be different due to constant change in coupon payments. This concepts will be explained throughout the ReadMe, so don't worry if you don't understand a thing yet.

### Face Value, Coupon Payment, Lifetime and Other Concepts to Know
When a bond issuer(seller) issues a new bond, it will have a face value, coupon payment, lifetime and other features.
#### Face Value
Face value is the price that bond issued. It is usually multiples of 100, a thousand, 10 thousand or 100 thousand dollars.
#### Coupon Payment
Coupon Payment is the payment amount you get in specific time intervals as a bondholder. This time interval is usually 6 months, in other words you get a interest income every 6 months for buying the bond(lending your money to bond issuer). However in this project this time interval is calculated as once a year. This will be mentioned more in weaknesses.
#### Lifetime
Lifetime is, well, lifespan of the bond. US Treasury bonds varies between a month to 30 years.
#### Interest Rate
Interest rate of a bond is the determinant factor of the coupon payment of that bond. Even though interest rates fluctates as the times passes, the initial interest rate (therefore the coupon payment) won't change once the bond is issued. This means a issued bond will pay the same coupon amount throughout its life time. However since the interest rates fluctates as the time goes by, a bond issued at a different time with the same face value may pay more or less interest.
#### Market Value of a Bond
Market value is a bit tricky concept. The sole purpose of this project is to calculate it afterall. Let's go with an example. Assume you have bond with the face value of 100 dollars that pays 5 dollars a year with the lifetime of 3 years. After you get the first payment you decided to sell the bond. At that time the interest rate for 2 year US Treasury bonds is 4%(We compare it with a 2 year bond since our bond has 2 years of lifespan left). If someone was to buy a newly issued 2 year US Treasury bond, he/she will get 8 dollar in coupon payment. However your bond pays 10 dollars for the same time interval. This means although your bonds face value is 100 dollars, its market value is higher since its coupon amount is higher compared to its peers. Since interest rates fluctates momentarly, so the market value of your bonds too.
#### Conclusion
Important concepts to understand bonds and the important of this projects explained. If you still don't understand a thing you might start to worry a bit.

## Why is this Project Useful?
With this code you can calculate a bonds current market value throughtout its lifetime. You can choose any date between January 1990 and December 2023, and the lifetime the bond between the values 1 to 10 (being included). The user only needs to give the start date and the lifespan. Coupon payment will be calculated automaticly calculated according to the interest rates for the day given by user.

## Data
Interest rates for 1, 2, 3, 5, 7, 10 year bonds from 1990 January to 2023 December is taken from "https://home.treasury.gov/". Interest rates for hypothetical 4, 6, 8 and 9 year bonds are derived from existing values using weighted average. For example, the interest rate for 9 year bond is the weighted average of 7 and 10 year bonds.

## Weaknesses
There are a lot of them.

#### Coupon Payment Time Interval
As mentioned above, a standart bond pays its coupon once every half year. However in this project it is assumed the bond makes a coupon payment every year. This causes a slight flaw that may boost of decrease the calculated value comparing to the real bond value.

#### Yet to Paid Coupon Payments Should Have Been Included in The Value
Assume you are holding a bond for 300 day since its last coupon payment and decided to sell it. The buyer must pay the coupon amount thats worth 300 day. Unfortunately adding this feature is quite a challenge. This causes a decrease in the calculated value comparing to the real bond value.

#### This Code Doesn't Have a Concept of Day
This code calculates the market price of a bond with whatever left of its lifespan. However, this lifespan is in years, instead of days.For example, if your bond is to mature in 1 day, its value is calculated like its lifespan is a year long. This causes flaws in calculations, especially near the end of coupon payment days.

#### Guessing Hypothetical Rates
No such thing like 8 year US Treasury bond exists. Therefore we need to guess the interest rates for the nonexisting bonds. Although the weighted average is fairly simple and effective guess technique, its a guess afterall.

## Conclusion
No sane person (including me) would use this code to manage their bond portfolio. However this code is able to give you a rough idea of a bonds market value throughout its lifetime using only historical values.
