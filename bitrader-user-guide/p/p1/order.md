# Order Modes in Bitrader

<figure><img src="../../../.gitbook/assets/Group 47302.png" alt="" width="563"><figcaption></figcaption></figure>

## **Limit Order**

In the Limit Order mode, the program will place an order based on the current latest mark price of the trading pair on the exchange, and the order will remain open until it is filled at the specified limit price.

* **Execution Risk**: Orders may not be filled immediately, especially during rapid market movements (e.g., when prices quickly move away from the set limit price).
* **Scenario**: Best used in stable market conditions where you want to control the price at which your order is filled.

## **Market Order**

In the Market Order mode, the program continuously places orders at the best available price, ensuring that the order is filled as quickly as possible, often at 100% completion.

* **For Long Positions**: The program will continuously place buy orders at the best available selling price. In a rising market, if the initial order is not fully filled, Bitrader will cancel any unfilled portions and place a new buy order at the higher current best price until the order is fully filled.
* **For Short Positions**: The program will continuously place sell orders at the best available buying price. In a falling market, if the initial order is not fully filled, Bitrader will cancel any unfilled portions and place a new sell order at the lower current best price until the order is fully filled.
* **Cost Consideration**: Orders in this mode generally have higher execution costs compared to Limit Orders due to price fluctuations.

## Planned Order

In the Planned Order mode, the program executes orders based on pre-set conditions for "entry price" and "exit price."

{% hint style="info" %}
* **Entry Price**: The program calculates the entry price based on a user-defined percentage increase or decrease from the current market price. This means placing an order at a price that is a% cheaper than the current price.
* **Exit Price**: The program calculates the exit price based on a user-defined percentage increase or decrease from the entry price. This reflects the desired profit margin of b% when closing the position.
{% endhint %}

>
>
> * **For Long Positions**: The program will place a buy order at a price lower by a% than the current price. When the market price drops to this level, the entry order is filled. After entering, the program will automatically place a sell order at a price higher by b% than the entry price. When the market price rises to this level, the exit order is filled.
> * **For Short Positions**: The program will place a sell order at a price higher by a% than the current price. When the market price rises to this level, the entry order is filled. After entering, the program will automatically place a buy order at a price lower by b% than the entry price. When the market price falls to this level, the exit order is filled.
> * **Cost Efficiency**: Orders in this mode tend to have lower execution costs compared to Market Orders, as they are planned based on anticipated price movements rather than immediate market prices.

<figure><img src="../../../.gitbook/assets/Pagination.png" alt=""><figcaption></figcaption></figure>
