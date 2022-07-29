# TezID Documentation

TezID consist of 3 components;

* [The Smart Contracts](https://github.com/tezid/contracts)
* [The Dapp](https://tezid.net)
* [The Oracle API](#the-oracle-api)

## The Smart Contracts

The TezID Smart Contracts are implemented in [SmartPy](https://smartpy.io/) and available as FOSS software [here](https://github.com/tezid/contracts).

There are two main contracts; the **controller** and the **store**.

### Controller

The controller is responsible for the logic interacting with TezID proofs. Limiting who and what proofs can be registered, cost, verifications, renewals etc. 

## Store

The store is responsible for holding the proof data. It also has available **views** and **entrypoints** for integration purposes.

## Entrypoints and view

Entrypoints and views for the TezID smart contracts is documented in the [contracts](https://github.com/tezid/contracts) repo.

## The Dapp

The TezID dapp, available at https://tezid.net, is used for interacting with the TezID smart contracts and Oracle API via a web browser. It is written in React. We have a goal to open source this component also, but it has not yet been a priority.

## The Oracle API

The TezID Oracle API is responsible for verification of proof data. It is here you can request a code for your email (as an example) and get your proof verified.

We have a goal to open source this component also, but it would require quite a bit of work to get it in a state where this would be secure, so it's not a priority atm.

The TezID Oracle is a RESTful HTTP(s) API.

## Endpoints

### GET /proofs/:address

GET the proofs for an `:address` in JSON format.

```
curl https://tezid.net/api/mainnet/proofs/tz1UZZnrre9H7KzAufFVm7ubuJh5cCfjGwam
```

### GET /profile/:address

GET the profile data for an `:address` in JSON format.

```
curl https://tezid.net/api/mainnet/profile/tz1UZZnrre9H7KzAufFVm7ubuJh5cCfjGwam
```

### GET /idz/:address

GET the $IDZ balance (and some xFarm related metrics) for an `:address` in JSON format.

```
curl https://tezid.net/api/mainnet/idz/tz1UZZnrre9H7KzAufFVm7ubuJh5cCfjGwam
```

### GET /prooftypes

GET a list of the available `prooftypes` in JSON format.

```
curl https://tezid.net/api/mainnet/prooftypes
```

enjoy.
