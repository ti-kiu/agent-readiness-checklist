# auth.md

YOURDOMAIN API Authentication

## Agent Auth

- **Status**: available
- **Available**: true
- **Capabilities**: oauth2
- **Identity Types**: anonymous, registered
- **Anonymous**:
  - **Status**: available
  - **Available**: true
  - **Credential Types**: access_token
  - **Endpoint**: https://YOURDOMAIN.com/api/auth/guest
  - **Rate Limit**: 10 requests/day
- **Registered**:
  - **Status**: available
  - **Available**: true
  - **Credential Types**: access_token, refresh_token
  - **Registration Endpoint**: https://YOURDOMAIN.com/auth/register
  - **Token Endpoint**: https://YOURDOMAIN.com/oauth/token

## OAuth 2.0 Authorization Server

- **Issuer**: https://YOURDOMAIN.com
- **Authorization Endpoint**: https://YOURDOMAIN.com/oauth/authorize
- **Token Endpoint**: https://YOURDOMAIN.com/oauth/token
- **JWKS URI**: https://YOURDOMAIN.com/.well-known/jwks.json

## Protected Resource

Resource metadata: https://YOURDOMAIN.com/.well-known/oauth-protected-resource
