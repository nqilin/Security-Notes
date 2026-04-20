# API Rate Limiting
## Core Concept
API rate limiting restricts the number of requests a client can make in a given time period. It prevents abuse, DDoS attacks, and resource exhaustion.

## Why It Matters
Unlimited API requests allow attackers to launch brute-force attacks, scrape data, or overload servers. Rate limiting is a simple but effective defense for APIs.

## How It Works (Theory)
1. Track requests per client (by IP, user ID, or API key).
2. Set a limit (e.g., 100 requests per minute).
3. Reject or delay requests that exceed the limit.
4. Return clear error messages (e.g., 429 Too Many Requests).

## Practical Example
FastAPI implementation (simplified):
```python
from fastapi import FastAPI, Request, HTTPException
from fastapi.middleware.cors import CORSMiddleware
from slowapi import Limiter, _rate_limit_exceeded_handler
from slowapi.util import get_remote_address
from slowapi.errors import RateLimitExceeded

limiter = Limiter(key_func=get_remote_address)
app = FastAPI()
app.state.limiter = limiter
app.add_exception_handler(RateLimitExceeded, _rate_limit_exceeded_handler)

@app.get("/api/data")
@limiter.limit("100/minute")
async def get_data(request: Request):
    return {"data": "secure data"}
```

## How to Defend / Secure
- Implement rate limiting for all public APIs.
- Use client-specific limits (API key > IP address).
- Return 429 status code with retry-after header.
- Gradually block repeat offenders.
- Exempt trusted clients (with proper authentication).

## Key Takeaways
1. Rate limiting prevents API abuse and DDoS.
2. Use API keys for more accurate client tracking.
3. Clear error messages help developers comply with limits.
