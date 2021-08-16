# Remove mediator role

1. ## What

   This is a proposal to eliminate the [mediator role](https://bisq.wiki/Mediator) as it exists today.

2. ## Why

   #### Privacy
   At present, with the opening of mediation, the mediator gets access to all the trade details from the traders in cause. Everything in the trade contract JSON is available to the mediator. And later to the arbitrator if arbitration is requested.

   Right now traders need mediators for guidance on the issues they may encounter and to suggest payouts releasing the funds in the multisig. We can separate these two functions (guidance and creation of payout transactions) and get rid of the mediator role.

   #### Guidance
   For most of the issues the trader can just reach out to the available support channels. Chances are that someone else has come across their issue. And if not, then some support agent can take a general description of their issue and guide them towards a solution. Without needing their sensitive information.

   In case some minor sensitive information may need to be shared then the trader can send a private message to the support agent.

   Furthermore we can focus on dividing the support agents in the following categories:
   + technical - for issues with the software
   + trade protocol - for doubts regarding Bisq's rules
   + payment methods - for troubles with the payment methods they are using

   #### Creation of payout transactions

   `BTC buyer ammount: y`
   `BTC seller ammount: x`

   That's all that there is to it. And this role can surely be handed to the traders themselves so they can solve their issues. And if they can't come to an agreement, arbitration awaits them.

3. ## How

   1. ### Add tools for the traders to negotiate a payout

      The traders would have a button in their Trader Chat window to suggest a payout to the other trader. Once the other trader accepts the offer the ticket is closed and the trade is moved to the History tab.

   2. ### Add the ability to export the trader's chat so it can be verified by a third party (arbitrator)

   3. ### Clarify steps for support

      1. Level 1
         1. the trader doesn't need to disclose any personal information
         2. the public support channel can help
      2. Level 2
         1. the trader needs to share some information about the transactions related to the trade
         2. the trader needs personal assistance from a support agent
      3. Level 3
         1. the trader needs to share logs which contain blockchain information regarding the trades made with that wallet
         2. the trader needs personal assistance from a support agent
      4. Level 4
         1. the trader needs to share all of the contract details with the arbitrator
         2. the trader needs personal assistance from the arbitrator

   4. ### Remove the mediator role