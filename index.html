const fs = require("fs");
const readline = require("readline");
const path = require("path");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

function clearScreen() {
  console.clear();
}

function prompt(question) {
  return new Promise((resolve) => {
    rl.question(question, (input) => resolve(input));
  });
}

async function main() {
  clearScreen();
  console.log("What do you want to do");
  console.log("\n1. Register an account");
  console.log("2. Login to account");
  const opt = parseInt(await prompt("\nYour choice: "), 10);

  if (opt === 1) {
    clearScreen();
    const ac = await prompt("Enter your account number:\t");
    const phone = await prompt("Enter your phone number:\t");
    const password = await prompt("Enter your new password:\t");
    const balance = 0;
    const filename = path.join(__dirname, `${phone}.dat`);
    fs.writeFileSync(
      filename,
      JSON.stringify({ ac, phone, password, balance })
    );
    console.log("\nAccount successfully registered");
  } else if (opt === 2) {
    clearScreen();
    const phone = await prompt("\nPhone number:\t");
    const pword = await prompt("Password:\t");
    const filename = path.join(__dirname, `${phone}.dat`);
    if (!fs.existsSync(filename)) {
      console.log("\nAccount number not registered");
    } else {
      const usr = JSON.parse(fs.readFileSync(filename, "utf8"));
      if (pword === usr.password) {
        console.log(`\nWelcome ${usr.phone}`);
        let cont = "y";
        while (cont === "y") {
          clearScreen();
          console.log("\n1. Check balance");
          console.log("2. Deposit an amount");
          console.log("3. Withdraw");
          console.log("4. Transfer the balance");
          console.log("5. Make payments");
          console.log("6. Change password");
          const choice = parseInt(await prompt("\nYour choice:\t"), 10);
          let amount;
          switch (choice) {
            case 1:
              console.log(
                `\nYour current balance is Kw.${usr.balance.toFixed(2)}`
              );
              break;
            case 2:
              amount = parseFloat(await prompt("\nEnter the amount:\t"));
              usr.balance += amount;
              fs.writeFileSync(filename, JSON.stringify(usr));
              console.log("\nSuccessfully deposited.");
              break;
            case 3:
              amount = parseFloat(await prompt("\nEnter the amount:\t"));
              usr.balance -= amount;
              fs.writeFileSync(filename, JSON.stringify(usr));
              console.log("\nSuccessfully withdraw.");
              break;

            case 4:
              const transferPhone = await prompt(
                "\nPlease enter the phone number to transfer to: "
              );
              const transferAmount = parseFloat(
                await prompt("\nPlease enter amount to transfer: ")
              );
              const transferFilename = path.join(
                __dirname,
                `${transferPhone}.dat`
              );

              if (!fs.existsSync(transferFilename)) {
                console.log("\nAccount number not registered");
              } else {
                const usr1 = JSON.parse(
                  fs.readFileSync(transferFilename, "utf8")
                );
                if (transferAmount > usr.balance) {
                  console.log("\nInsufficient balance");
                } else {
                  usr1.balance += transferAmount;
                  fs.writeFileSync(transferFilename, JSON.stringify(usr1));
                  console.log(
                    `\nYou have successfully transferred Kw.${transferAmount.toFixed(
                      2
                    )} to ${transferPhone}`
                  );
                  usr.balance -= transferAmount;
                  const userFilename = path.join(__dirname, `${usr.phone}.dat`);
                  fs.writeFileSync(userFilename, JSON.stringify(usr));
                }
              }
              break;
              case 5:
                const paymentPhone = await prompt("\nPlease enter the phone number to pay to: ");
                const paymentAmount = parseFloat(await prompt("\nPlease enter amount to pay: "));
                const paymentFilename = path.join(__dirname, `${paymentPhone}.dat`);
              
                if (!fs.existsSync(paymentFilename)) {
                  console.log("\nAccount number not registered");
                } else {
                  const usr1 = JSON.parse(fs.readFileSync(paymentFilename, "utf8"));
                  if (paymentAmount > usr.balance) {
                    console.log("\nInsufficient balance");
                  } else {
                    usr1.balance += paymentAmount;
                    fs.writeFileSync(paymentFilename, JSON.stringify(usr1));
                    usr.balance -= paymentAmount;
                    fs.writeFileSync(filename, JSON.stringify(usr));
                    console.log(`\nYou have successfully paid Kw.${paymentAmount.toFixed(2)} to ${paymentPhone}`);
                  }
                }
                break;
            case 6:
              const newPassword = await prompt(
                "\nPlease enter your new password: "
              );
              usr.password = newPassword;
              const userFilename = path.join(__dirname, `${usr.phone}.dat`);
              fs.writeFileSync(userFilename, JSON.stringify(usr));
              console.log("\nPassword successfully changed");
              break;

            default:
              console.log("\nInvalid option");
              break;
            // ... Implement other cases similarly ...
          }
          cont = await prompt(
            "\nDo you want to continue transaction? Press [y/n]: "
          );
        }
      } else {
        console.log("\nInvalid password");
      }
    }
  }
  rl.close();
}

main();
