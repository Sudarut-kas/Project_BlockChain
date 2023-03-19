# BlockChain_Project_Group11
Final project, Raffle system using varifiable random function, Skoltech 2023

# Solidity session
This code was written to create a lottery system in which users could send money and a winner would be chosen at random. Which owner can set a period for selling in a lottery, and if users want to play after the period has expired, the system will reject them. After the closed period, a random winner will be selected by owner. Randomness was implement by VRF on Oracle chainlink.

# How to run
- Using Remix-Ethereum platform by using 0.8.0+complier

- Using Sepolia Chain Link VRF \
 VRFConsumerBase(0x8103B0A8A00be2DDC778e6e7eaa21791Cd364625, >> coordinator \
                 0x779877A7B0D9E8603169DdbD7836e478b4624789) >> link\
                {keyHash = 0x474e34a077df58807dbe9c96d3c009b23b3c6d0cce433e59bbf5b34f823bc56c; \
                 fee = 0.25 * 10 ** 18 ; \
                 admin = msg.sender;} \
 in this part you can change to others testnet i.e. Goerli, BNB \
 
 # Step to play
 1. Ower create lottery by click on createLottery button 
    - input ticket price(lottery price)
    - input second(time period for lottery in seconds)
    
 2. Owner and users can enquiry data about lottery \
    getLotteryCount: Input lotteryID, to see how many participants are playing in lotteryID \
    getLottery: Input lotteryID, to see data in tuple \
                - uint256: lotteryId \
                - address[]: participants \
                - uint256: prize \
                - uint256: ticketPrice \
                - address: winner \
                - boolean: isFinished \
                - uint256: endDate 

    ![Owner creates the lotteries and Players can participate in avaialble lotteries.](https://github.com/waralak/Project_BlockChain/blob/main/readme_pics/11.PNG)
                
 3. Users play by click on participate button 
    - input lotteryID 
    ![Players can check total amount of lotteries in the system and details.](https://github.com/waralak/Project_BlockChain/blob/main/readme_pics/12.PNG)
    
 4. Owner can get the winner by click on declareWinner 
    - input lotteryID
    and see details of the winner in getLottery
    ![Owner can get the winner.](https://github.com/waralak/Project_BlockChain/blob/main/readme_pics/13.PNG)
    
