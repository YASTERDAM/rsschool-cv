# Ivan Chaliadzinski
### Contacts
- **phone**: +375(29)681-19-09;
- **email**: ivan.drozd26062606@gmail.com;
- **telegram**: @Yasterdam;

### Summary
My main goal is to get a job as a front-end developer and make friends. All my life is connected with Math and Programming, that's why it's close to me and I chose this specialty.

### Skills
Basic knowledge of HTML, CSS, JavaScript, Git & GitHub, C++, C, MySQL, Java(Android development).
### Latest code example
```javascript
$(document).ready(function() {
    let funds = 50;
    let round = 0;
    let bet, face;
    while (funds > 1 && funds < 100) {
        let winnings = 0;
        round++;
        console.log(`round: ${round}`);
        console.log(`start money: ${funds}`);
        let bets = { crown: 0, anchor: 0, heart: 0, diamond: 0, spade: 0, club: 0 };
        let totalBet = rand(1, funds);
        if (totalBet === 7) {
            totalBet = funds;
            bets["heart"] = totalBet
        } else {
            let buffer = totalBet;
            do {
                bet = rand(1, buffer);
                face = randFace();
                bets[face] = bets[face] + bet;
                buffer = buffer - bet;
            } while (buffer > 0);
        }
        funds = funds - totalBet;
        console.log(`\tbets: ` + Object.keys(bets).map(face => `${face}: ${bets[face]}pence`).join(', ')+`(total:${totalBet}pence)`);
        let hand = [];
        for (let roll = 0; roll < 3; roll++) {
            hand.push(randFace());
        }
        console.log(`\thand: ${hand.join(`, `)}`);
        for (let die = 0; die < hand.length; die++) {
            face = hand[die];
            if (bets[face] > 0) {
                winnings = winnings + bets[face];
            }
            funds = funds + winnings;
        }
        console.log(`\ttotal winning: ${winnings}`);
    }
    console.log(`total funs: ${funds}`);
})
function rand(m, n) {
    return m + Math.floor((n - m + 1) * Math.random());
}
function randFace() {
    return ["crown", "anchor", "heart", "spade", "club", "diamond"][rand(0, 5)];
}
```
### Experience
- courses of C programming language;
- Rolling Scopes School practice;

### Education
- Belarusian State University of Informatics and Radioelectronics(2018);

### English
Upper-Intermediate;