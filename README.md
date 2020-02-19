# Cashfree Bank Validation Integration Kit for Python 

Below is an integration flow on how to use Cashfree's payouts sdk.
Please go through the payout docs [here](https://docs.cashfree.com/docs/payout/guide/)
<br/>
This kit is linked to the Bank Validation flow. Go [here](https://dev.cashfree.com/payouts/integrations/bank-validation) to get a better understanding.
<br/>

## Functionalities

The following kit contains the following functionalities:
    <ol>
    <li> init: to initialise the sdk.
    <li> Validations.bank_details_validation: to verify bank account.
    </ol>
<br/>
You can get more information on the python sdk [here](https://github.com/cashfree/cashfree-sdk-python).

## Build Steps

follow the following build steps to compile the Integration kit:
  1. Download the code and cd into the directory containing the code.
  2. install the following dependancy Cashfree python sdk
  ```
  pip3 install git+https://github.com/cashfree/cashfree-sdk-python.git
  ```
## Set Up

### Pre Requisites:
The following kit uses information stored in a app.py file. Before running the code for the first time open the app.py file
and add the relevant details:
  1. ClientId: This is a unique Identifier that identifies the merchant. For more information please go [here](https://dev.cashfree.com/payouts/integrations/pre-requisites#credentials).
  2. ClientSecret: Corresponding secret key for the given ClientId that helps Cashfree indentify the merchant. For more information please go [here](https://dev.cashfree.com/payouts/integrations/pre-requisites#credentials).
  3. Environment: Enviornment to be hit. The following values are accepted prod: for production, test: for test enviornment. Pass this parameter to the init function

### IP Whitelisting:

Your IP has to be whitelisted to hit Cashfree's server. For more information please go [here](https://dev.cashfree.com/payouts/integrations/pre-requisites#ip).

### Bank Details:

The following kit needs bank account details to validate the bank account. For a list of required fields go [here](https://dev.cashfree.com/api-reference/payouts-api#bank-verification)
<br/>
The kit picks up the bank account details from the app.py file as the object passed to bank_details_validation method. Required fields are:
  1. name: name of the account to be verified.
  2. phone: phone number of the account holder.
  3. bankAccount: bank account to be validated.
  4. ifsc: ifsc of corresponding bank account.


## Usage

Once the app.py file is setup you can run the executable, to run the entire flow. Authorise and validate bank account. 

run the following command in the terminal to run the script:
```
  python app.py
```

You can change the necessary values in the config file as per your app.py and re run the script whenever needed.

## Doubts

Reach out to techsupport@cashfree.com in case of doubts.
 


