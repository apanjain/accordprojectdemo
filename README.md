[![accord project](https://img.shields.io/badge/powered%20by-accord%20project-19C6C8.svg)](https://www.accordproject.org/)

# Accord Project Demo
 This project provides a simple template for a person's data, and determines his/her age from given DoB.

## Setup
- Clone this repository
- cd into the directory

```shell
cd accordprojectdemo/
```

- run the following command
```shell
npm install
```

## Usage
- There is sample contract data present in sample.md.
- Run the following command and the output will be a JSON object containing age value.
```shell
npx cicero trigger
```

- To extract the data from contract text.
```shell
npx cicero parse --output data.json
```

- To update the contract text data there are two ways
  - Change the data directly in text/sample.md OR
  - Update data.json then draft the contract text using
  ```shell
  npx cicero draft --output text/sample.md
  ```

# Description
## Text
- This is a contract written in natural language by lawyers.
- This is what guides the logic.
- The data fields required to process a contact logic are placed here in placeholders which are parsed directly to models.
- There are two parts to this.
  - grammer.tem.md where we define our contract structure. The final contract is written in the same syntax.
  - There is another markdown file (in our case sample.md) which is our actual contract. This is same as grammer file just replacing the placeholders.

## Models
- This is what unites Logic and Text.
- Data from text is parsed into specific data types mentioned.
- These fields are then accessible in logic.
- model/model.cto is where we define our models. It can import other custom models.

## Logic
- Here lies the logic of our contract.
- We send request to one or more clauses which processes the logic and respond with a json data.
- The logic written should follow the contact text strictly.
- logic/logic.ergo is where we write our logic.
- For more info see the [documentation](https://docs.accordproject.org/)