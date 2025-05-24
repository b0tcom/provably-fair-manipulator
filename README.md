# Provably Fair Exploiter (Case Battle Simulator)

**For security research, education, or authorized fairness audit only!**

---

## What is this?

A simple JS tool to simulate the exact outcome of case battle rounds/tickets using *provably fair* logic, given the `serverSeed`.  
No dependencies except the one provided CDN (`seedrandom`). No ES modules. Runs directly in any modern browser’s DevTools console.

---

## Usage

### 1. Load the Script

- Open the casino/game website in your browser (Edge/Chrome/Firefox).
- Open **DevTools Console** (`F12` or right-click → Inspect → Console).
- Paste the **entire contents of `provably_fair_exploiter.js`** into the console and hit **Enter**.
- Wait for the `Provably Fair Exploiter READY` message.

---

### 2. Run Simulations

#### Create an exploiter instance
```js
const exploiter = new ProvablyFairExploiter();
exploiter.simulateCaseBattle(
  'YOUR_SERVER_SEED',   // string: the revealed or candidate server seed
  5,                    // number: number of rounds/cases
  '2vs2',               // type: '1vs1', '1vs1vs1', '2vs2', '3vs3'
  false                 // isOld: use false unless the site is running the legacy battle algorithm
);
