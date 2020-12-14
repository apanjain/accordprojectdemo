[![accord project](https://img.shields.io/badge/powered%20by-accord%20project-19C6C8.svg)](https://www.accordproject.org/)

# Accord Project Demo
 This project provides a simple template for a person's data, and determines his/her age from given DoB.

## Setup
- Install [Cicero](https://docs.accordproject.org/docs/started-installation.html).
- Clone this repository.
- cd into the directory
```shell
cd accordprojectdemo/
```
- Run the following command
```shell
npm install
```

## Usage
- There is sample contract data present in sample.md.
- Run the following command and the output will be a JSON object containing age value.
```shell
cicero trigger
```

- To extract the data from contract text.
```shell
cicero parse --output data.json
```

- To update the contract data there are two ways
  - Change the data directly in text/sample.md
  - Update data.json then draft the template using
  ```shell
  cicero draft --output text/sample.md
  ```
