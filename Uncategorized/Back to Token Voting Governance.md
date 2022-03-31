A few months ago, Vitalik wrote a piece called [[Moving beyond coin voting governance]] which outlined the types of vulnerabilities associated with highly fungible and often times market valued assets as a delegator for voting rights. I think his analysis is an excellent example of why the current model of token governance is flawed, but I disagree with his implied conclusion (That he doubled down on in ETHDenver 2022) that all token voting should stop. For corporate like structures that are owned by the people that provide value in it, utilizing a fungible asset that can weigh in to how valuable a specific entity has been to a community at a current point in time is extremely useful. I want to reintroduce the criticism of Vitalik in token voting in the context of the current token design frameworks, describe why his criticism of it is based on foundations of tokens being built as financial instruments based off monetary policy, and introduce a framework for creating tokens which are used to align incentives, rather than communicate information around market conditions.
Weighted voting is a system that allows for actors in a system to signal (and automatically execute in the case of on-chain governance) their preference in a way that is aligned with people that have provided value in that system. Actually, it is a well studied system, and obviously the one that is preferred by corporations and provides an extremely useful metrics for signaling value within the system. There has been a few talks about moving DeGov away from fungible tokens and towards NFTs, and a lot of experiments have appeared in that space with Proof-of-personhood, poaps, and other measures to improve sybil-resistance. I do think that these measures can be introduced to token governance systems to make token voting more effective. However, their effectiveness will only be as good as their ability to combine with weighted voting - which returns us to the token voting systems we are seeing today.

There are three main reasons that token voting is so problematic today:
	-  We are designing government's structures as though they are monetary policies
	-  Monetary polices are prioritizing the stability of price, while governance should prioritize signaling the amount of value that a contributor has given to a community
	- Removing the priority we give towards unit price enables better governance primitives

## Governance Policy is not Monetary Policy
Seems like an obvious statement. 

However, if you take a moment to look at the governance policy of some of the most popular DAOs you'll see a lot of similarities:
ENS contract which you can find [here](https://etherscan.io/address/0xc18360217d8f7ab5e7c516566761ea12ce7f9d72#code)
(This is simplified to only show the things to do with the token issuance)
```java
contract ENSToken is ERC20, ERC20Permit, ERC20Votes, Ownable {
    uint256 public constant minimumMintInterval = 365 days;
    uint256 public constant mintCap = 200; // 2%

    uint256 public nextMint; // Timestamp
	
    constructor() {
        _mint(msg.sender, supply);
        nextMint = block.timestamp + minimumMintInterval;
    }
```

And further down we can see the mint function:
```java	
	/**
     * @dev Mints new tokens. Can only be executed every `minimumMintInterval`, by the owner, and cannot
     *      exceed `mintCap / 10000` fraction of the current total supply.
     * @param dest The address to mint the new tokens to.
     * @param amount The quantity of tokens to mint.
     */
    function mint(address dest, uint256 amount) external onlyOwner {
        require(amount <= (totalSupply() * mintCap) / 10000, "ENS: Mint exceeds maximum amount");
        require(block.timestamp >= nextMint, "ENS: Cannot mint yet");

        nextMint = block.timestamp + minimumMintInterval;
        _mint(dest, amount);
    }
```
A summary of what is happening is this: 
On launch, there is an initial supply of 100,000,000 tokens, and every year, the supply can be increased at a rate of 2% inflation. I don't know where this idea came from, but I would venture to assume that it came from the 2% marker of that central banks give as an ideal rate[(1)](https://www.federalreserve.gov/faqs/what-economic-goals-does-federal-reserve-seek-to-achieve-through-monetary-policy.htm)  for a country's monetary supply. The reasons they have for doing so is that it encourages spending by individuals, keeps interest rates stable, and have room to be managed in an economic downturn[(2)](https://www.federalreserve.gov/faqs/economy_14400.htm). The merits of this argument should be evaluated on those metrics, but the question is this: are those the metrics we need to evaluate when discussing governance models?
## Governance Should Prioritize Contributors Value at a Given Snapshot in Time
So if we accept that prioritizing interest rates, consumer spending, and managing economic downturns might not be the best thing to prioritize for governance, what then should we be prioritizing? I have a proposal for that, which is to make governance tokens a signal for the current rate of value given to a community. Let me explain.
Current models for tokens are strange, they are a mixture between something 'like' equities, and something 'like' money. However, they are kind of bad at both. Voting Shares in a corporation are useful because people that are more 'invested' in a company have more of a say, and if you control more than half of a corporation's equity, you are effectively in charge of making decisions for that corporation. The thing about equity shares with voting power is that they are 



Notes: