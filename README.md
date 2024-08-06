# Duckduckgo AI Chat Service

English | [中文](./README_CN.md)

Provide an OpenAI-compatible API for [Duckduckgo AI Chat](https://duckduckgo.com/aichat) that can be used for free with gpt-4o-mini.

## Deploy

### Deno

```sh
# Run directly
deno run --allow-env --allow-net --unstable https://raw.githubusercontent.com/mumu-lhl/duckduckgo-ai-chat-service/main/main.ts

# Run after installation
deno install -g --allow-env --allow-net --unstable -n duckduckgo-ai-chat-service https://raw.githubusercontent.com/mumu-lhl/duckduckgo-ai-chat-service/main/main.ts
duckduckgo-ai-chat-service
```

### Deno Deploy

#### Command line

```sh
git clone https://github.com/mumu-lhl/duckduckgo-ai-chat-service --depth 1
deno install -A jsr:@deno/deployctl
deployctl deploy
```

#### Web

Fork this project, then visit <https://dash.deno.com> and create new project after loging in.

## Configuration

Configuration using environment variables:

* TOKEN - Limit the tokens that can access the API, if you don't fill in, any token can access the API.
* LIMIT - limit the request rate per second, default is 2
* CLEAN_CACHE_CRON - how many hours to clean up the cache, default is 1

## Usage

Just change the base url of the place where you need to use the OpenAI API to the one you deployed.
