CIMB is a digital bank that offers GSave and UpSave savings accounts.   As with a typical Savings Account, it contains accountNumber, accountName, and a balance for that account.

The typical savings account offers an interest rate of 1%.
The benefits of the typical savings account is the same with the "Standard Savings Account" as compared to other banks.

The GSave account offers an interest rate of 2.5%.
Benefits include the "Standard Savings Account" plus access to "GCash transfer".

The UpSave account offers the highest interest rate of 4.0%.
Benefits include the "Standard Savings Account" plus "with Insurance".


Develop a decorator pattern approach that will implement the given UML diagram:

![DECORATOR PATTERN](https://github.com/vjpjulia/Assignment-10/blob/main/Decorator%20Pattern.png)


The content of your Cimb.java should ONLY contain the following codes with the exception of inserting your own package name :


public class BankApp {

	public static void main(String[] args) {
		
		SavingsAccount account = new SavingsAccount();
		
		account.setAccountNumber(1234);
		account.setAccountName("Juan Dela Cruz");
		account.setBalance(10000.0);
		
		System.out.println(account.showInfo());
		System.out.println("Account type: " + account.showAccountType());
		System.out.println("Interest rate: " + account.getInterestRate());
		System.out.println("New balance: " + account.computeBalanceWithInterest());
		System.out.println("Benefits: " + account.showBenefits());
		
		System.out.println("----------------------");
		
		GSave gSave = new GSave(account);
		System.out.println(gSave.showInfo());
		System.out.println("Account type: " + gSave.showAccountType());
		System.out.println("Interest rate: " + gSave.getInterestRate());
		System.out.println("New balance: " + gSave.computeBalanceWithInterest());
		System.out.println("Benefits: " + gSave.showBenefits());
		
		System.out.println("----------------------");
		
		UpSave upSave = new UpSave(account);
		System.out.println(upSave.showInfo());
		System.out.println("Account type: " + upSave.showAccountType());
		System.out.println("Interest rate: " + upSave.getInterestRate());
		System.out.println("New balance: " + upSave.computeBalanceWithInterest());
		System.out.println("Benefits: " + upSave.showBenefits());
	}
}


you should display the following output:

Account number: 1234
Account name: Juan Dela Cruz
Balance: 10000.0
Account type: Savings Account
Interest rate: 0.01
New balance: 10100.0
Benifits: Standard Savings Account
----------------------
Account number: 1234
Account name: Juan Dela Cruz
Balance: 10000.0
Account type: GSave
Interest rate: 0.025
New balance: 10250.0
Benifits: Standard Savings Account, GCash Transfer
----------------------
Account number: 1234
Account name: Juan Dela Cruz
Balance: 10000.0
Account type: UpSave
Interest rate: 0.04
New balance: 10400.0
Benifits: Standard Savings Account, With Insurance


Description of the following methods

showAccountType() - Either returns "Savings Account", "GSave" or "UpSave"
getInterestRate() - Either returns 1% for Savings Account; 2.5% for GSave; 4.0% UpSave
getBalance() - Returns the balance of the account set.
showBenefits() - Either returns "Standard Savings Account" for Savings Account;
		    benefits offered by savings account + "GSave Transfer";
                            benefits offered by savings account + "With Insurance";
computeBalanceWithInterest() - returns new balance by computing the balance plus the interest depending on the interest rate.
showInfo() - Returns details of account number, account name, and balance.

BankAcountDecorator must be an interface.

Follow instructions.  You are not allowed to insert other methods except what is stated in the diagram (setters and getters are allowed).

