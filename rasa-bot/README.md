# 3cs-bot

A Rasa bot that can generate and rephrase responses on the fly using LLMs

## Deploying

To deploy and run the bot, `docker` and `docker-compose` are required.

1. Clone the repository and do `cd rasa-bot`
2. create .env file and add your OpenAI API key under the `OPENAI_COMPLETIONS_API_KEY` key
3. Go to the project root directory and run `docker compose up -d` to run everything
4. The widget should be available @ http://localhost:80

## Talking to the bot

The bot is a demo 3CS web design inquiry assistant that can do the following:

- Greet users
- Handle web design inquiries
- Gather budget information
- Gather project deadline information
- Provide responses based on budget and deadline
- Say welcome
- Say goodbye

All the bot responses are generated or rephrased using the OpenAI GPT-3 `gpt-3.5-turbo` completions model.

In case the rate limit is met (3 requests within a minute last I checked), the bot will utter the default rephrase response.
