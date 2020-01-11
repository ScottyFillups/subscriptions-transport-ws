# subscriptions-transport-ws

My hacky fork of `subscriptions-transport-ws@0.5.4`.

I did this because he wants his GraphiQL playground to work with subscriptions.

`graphiql-subscriptions-fetcher` only works with `<=0.5.4`, but `0.5.4` still uses `Sec-WebSocket-Protocol: graphql-subscription` instead of `Sec-WebSocket-Protocol: graphql-ws`.

My server requires the subprotocol to be `graphql-ws`, so I either had to:
* Make `graphiql-subscriptions-fetcher` comply with the new `subscriptions-transport-ws` interface
* Make my server non-compliant to the GraphQL specification
* Just replace a string in `subscriptions-transport-ws@0.5.4`

I'm really lazy, so I picked the last one :)
