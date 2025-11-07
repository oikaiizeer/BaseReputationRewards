# 🏆 Base Reputation Rewards

A gamified on-chain reputation system built for Base blockchain that rewards user engagement and community participation.
done 
## ✨ Features

- **Daily Check-ins** - Earn reputation points every day with streak multipliers
- **Peer Endorsements** - Community members can endorse each other
- **Achievement Badges** - Unlock badges as you progress through reputation tiers
- **Level System** - Automatically level up based on reputation points
- **Streak Rewards** - Get bonus points for consecutive daily check-ins
- **Leaderboard Ready** - Built-in support for tracking top contributors

## 🎮 How It Works

### Earning Reputation Points

| Action | Points | Requirements |
|--------|--------|--------------|
| Daily Check-in | 10 + streak bonus | Once per day |
| Perform Action | 5 | Any time |
| Receive Endorsement | 25 | From users with 50+ points |
| Streak Bonus | 2 × streak days | Consecutive check-ins |

### Badge Tiers

1. **Newcomer** - 0 points (Welcome!)
2. **Active Member** - 100 points
3. **Trusted Contributor** - 500 points
4. **Community Leader** - 1,000 points
5. **Legend** - 5,000 points

### Level System

Your level increases automatically: `Level = (Reputation Points / 100) + 1`

## 🚀 Deployment

### Prerequisites

- Node.js v18+
- Foundry or Hardhat
- Base testnet/mainnet RPC URL

### Deploy to Base

```bash
# Using Foundry
forge create --rpc-url <BASE_RPC_URL> \
  --private-key <PRIVATE_KEY> \
  src/ReputationRewards.sol:ReputationRewards

# Using Hardhat
npx hardhat run scripts/deploy.js --network base
```

### Contract Addresses

- **Base Mainnet**: `TBD`
- **Base Sepolia Testnet**: `TBD`

## 📖 Usage Examples

### Daily Check-in

```solidity
// Call once per day to earn points
reputationRewards.checkIn();
```

### Record an Action

```solidity
// Log any community action
reputationRewards.performAction("Participated in governance vote");
```

### Endorse Another User

```solidity
// Requires 50+ reputation points
reputationRewards.endorseUser(0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb);
```

### Check User Profile

```solidity
(uint256 reputation, uint256 level, uint256 streak, uint256 badges) = 
  reputationRewards.getUserProfile(userAddress);
```

### Verify Badge Ownership

```solidity
bool hasLegendBadge = reputationRewards.hasUserUnlockedBadge(userAddress, 4);
```

## 🎯 Use Cases

- **Community DAOs** - Reward active governance participants
- **DeFi Protocols** - Gamify user engagement and liquidity provision
- **Social Platforms** - Build on-chain reputation systems
- **Gaming Projects** - Track player achievements and progression
- **NFT Communities** - Reward collectors and contributors

## 🛠️ Development

### Build

```bash
forge build
```

### Test

```bash
forge test
```

### Gas Report

```bash
forge test --gas-report
```

## 🔐 Security Considerations

- Daily check-ins are time-locked to prevent spam
- Users cannot endorse themselves
- Each user can only endorse another user once
- Minimum 50 reputation points required to endorse others
- Owner-only functions for adding custom badges

## 🌟 Future Enhancements

- [ ] NFT badges that can be displayed in wallets
- [ ] Reputation decay for inactive users
- [ ] Seasonal leaderboards with rewards
- [ ] Integration with Base Name Service
- [ ] Reputation staking mechanisms
- [ ] Cross-protocol reputation bridges
- [ ] Achievement quests and challenges

## 📊 Why Base?

Base offers:
- **Low gas fees** - Affordable for frequent interactions
- **Fast finality** - Quick confirmation times
- **EVM compatible** - Easy to develop and integrate
- **Growing ecosystem** - Active community and projects

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Links

- [Base Documentation](https://docs.base.org)
- [Base Block Explorer](https://basescan.org)
- [Base Bridge](https://bridge.base.org)

## 💬 Community

- Twitter: [@YourProject]
- Discord: [Join our server]
- Telegram: [Join our channel]

---

**Built with ❤️ for the Base ec
