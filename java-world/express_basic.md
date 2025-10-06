**Express Routes Cheat Sheet:**
```markdown
# Express Routes Quick Reference

## Basic Route Structure
app.METHOD(PATH, HANDLER)

## Common Methods
GET    - Retrieve data
POST   - Create data
PUT    - Update data
DELETE - Remove data

## Response Methods
res.json()    - Send JSON
res.send()    - Send text/HTML
res.status()  - Set status code
res.redirect()- Redirect to URL

## Request Data Sources
req.params - URL parameters (/users/:id)
req.query  - Query string (/users?active=true)
req.body   - Request body (needs body-parser)
```
