# Credit Card Travel Bot

This is an example Rasa CALM chatbot for a travel related credit card customer. Some example skills:

- Handle FAQ's using enterprise search
- Account balance checker
- Request recent purchase info
- Making payments
- Get special offers
- Review recent charges
- Hear payment due date
- Check available credit
- Check Membership Rewards

## Setup

Requires `3.7.0` or later

```sh
export RASA_PRO_LICENSE=xyzzy
export OPENAI_API_KEY=xyzzy
rasa train --domain domain/
rasa test e2e e2e_tests
```

## To talk to the bot

First start the action server:

```bash
rasa run actions
```

You then have several options talk to the bot:

- `rasa inspetct`     (recommended)
- `rasa shell`
- `make rasa-run`, then open `index.html` in the browser
  - This option sends an initial payload upon connect & it allows for some styling in case of demos.

## Example LLM Flows

- search for hotels
- check the user's account balance

## Testing Enterprise Search

The demo loads credit card travel related FAQ's. The source documents are in the `/docs` directory of this repo.

Here are some example questions:

- What hotel credits are available
- Do I have access to airport lounges
- Are there any airline fee credits
- Can points be used to upgrade flights
- Can I use points to book travel for others
