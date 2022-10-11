# Requirements

Please find below the Solidity tech test.

The deadline is: October 13, 2022 at the same time. 

If you have some techical questions, please send a message to tiago.bem@realfevr.com and/ or pedro.febrero@realfevr.com

If you have questions about the recruitment process, talk to me.

Please confirm me the receipt of this message today.

Thanks and good work! 

Ana Vieira.



___

Solidity Test

This is a brief test where you can show-case your skills on solidity development.

Mission Overview

Deliver the requested contract, described below, within a week. This means you have 7 days.

 
Mission Details

Build the following smart contract using the latest solidity version.

NFT Lottery

 
The NFT Lottery contract will receive a token (ERC20), mint and transfer to the msg.sender a ticket (ERC1155), sell a portion of the received ERC20 for another ERC20 (swap) and finally send the swapped funds to an address.

 
The NFT Lottery contract should draw a random winner from 10 ticket sales. This means that after 10 tickets are sold, one of the buyers [1-10] will randomly be rewarded with an NFT they can mint. 

The contract should store the following events:

 
Ticket sale,

Total Tokens swapped per saleId,

Lottery winner per lotteryId.

 
Suggested NFT Lottery contract functions

 
buyTicket - holds the saleId, ticket price, total tickets, fee

ticketDetails - ticketId, address msg.sender

createLottery - LotteryId

winnerNFT - TicketIds [range]

vaultAddress - address

approvedERC20 - address

Hi Tiago,

Regarding to assessment, I have some questions and want to confirm requirements.
You described on requirements like below.
"This means that after 10 tickets are sold, one of the buyers [1-10] will randomly be rewarded with an NFT they can mint. "
"buyTicket - holds the saleId, ticket price, total tickets, fee"
1. Can one buyer buy more than 2 tickets? If so, buyer can buy 11 tickets? If not, what is the meaning for 'total tickets' param?
2. What for fee param? Should I implement specific calculation with fee value?
3. "Winner will be rewarded with an NFT they can mint", could you describe more detail of this requirement?
4. Regarding to lottery concept, after 10 tickets are sold and winner is determined, one lottery round is completed then new lottery round is started, am I right?
5. "sell a portion of the received ERC20 for another ERC20 (swap) and finally send the swapped funds to an address.", swap rate of two ERC20 tokens are 1:1, right?
6. Swapped funds should be stored in vaultAddress, right?
7. Let me know about approvedERC20 token. Is it swapped token or the token that needs to be swapped?

I think if detail is specified, I can complete this assessment within 2 ~ 3 hours.

Sorry to ask for many questions.
Look forward to hearing from you soon so that I can complete assessment and submit asap.

Thanks,

Michael

1. Buyer can buy unlimited amount of tickets (for simplicity sake)
2. Yeah let's say 10% fee that goes to another address (vaultFee). So user purchases ticket, 90% goes to vaultLottery and 10% to vaultFee. The swap of tokens happens only for the vaultLottery, so 90%; the other 10% can remain in the original token. This was not on the original request but we can add it, if you don't mind.
3. Once a winner is randomly chosen they can use the same contract to mint an nft - call it NFTwinner and it only holds the nftId (1,2,3, etc) 
4. Absolutely correct
5. swap rate can be 2:1
6. Yes funds can be stored at vaultLottery
7. ApprovedERC20 Just for the token that is being swapped

We can set the price of each ticket = 1,000 tokens. 

Thanks for all the questions, happy to clarify any further questions.
