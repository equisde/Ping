# Ping
Ping releases
This Repo is only for Ping releases


Telegram group= 

PING Hybrid PoW/PoS Masternodes With darksend
´´´
block time= 30 seconds
min stake age= 8 hour 
#define BLOCK_START_MASTERNODE_PAYMENTS_TESTNET 3700 // Testnet Masternode payments enabled block 81k5
#define BLOCK_START_MASTERNODE_PAYMENTS 342000 //Mainnet Masternode payments not enabled until block 342k
static const int64_t DARKSEND_COLLATERAL = (1000*COIN); // 1,000 PNG
static const int64_t DARKSEND_FEE = (0.010000*COIN); //0.01 PNG
static const int64_t POOL_FEE_AMOUNT = (0.1*COIN); //0.1 PNG
static const int64_t DARKSEND_POOL_MAX = (11000*COIN); //11,000 PNG
static const int LAST_POW_BLOCK = 2000000;
static const int FAIR_LAUNCH_BLOCK = 270; // Last Block until full block reward starts
static const unsigned int MAX_BLOCK_SIZE = 1000000; // 1MB block hard limit, double the size of Bitcoin
static const int64_t MAX_MONEY = 1000000000 * COIN; // 1,000,000,000 PNG Ping Max v1.0.0
static const int64_t COIN_YEAR_REWARD = 0.06 * COIN; // 6% per year

static const int64_t MAINNET_POSFIX = 200001; //Mainnet Proof of Stake update not enabled until block 201k

{
	int64_t nSubsidy = 1 * COIN;

	if (pindexBest->nHeight == 1)
		nSubsidy = 60000000 * COIN;  // Premine	
	else if (pindexBest->nHeight <= FAIR_LAUNCH_BLOCK) // Block 270, Instamine prevention
        nSubsidy = 1 * COIN/2;	
	else if (pindexBest->nHeight <= 3398) // V1.0.0 fork in block 3398/ Block 3398 ~ 6,796k BZl
		nSubsidy = 2 * COIN;
	else if (pindexBest->nHeight <= 1000000) // V1.0.0 / Block 1m ~ 993,204k PNG
		nSubsidy = 1 * COIN;	
	else if (pindexBest->nHeight <= 1500000) // V1.0.0 / Block 2m ~1m PNG
		nSubsidy = 1 * COIN;
	else if (pindexBest->nHeight <= 2000000) // V1.0.0 / Block 3m ~1m PNG
		nSubsidy = 1 * COIN;		
    else if (pindexBest->nHeight > LAST_POW_BLOCK) // Block 1.5m
		nSubsidy = 0; // PoW Ends ~ 4,500,000 Total PNG Mined via PoW
}


   ´´´               
