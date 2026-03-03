# identity-effectful

A Haskell Stack template for DDD + Effectful based Identity (auth) backend.

## Create Project

```bash
stack new my-project /path/to/identity-effectful.hsfiles
```

Template variables can be specified with the `-p` option.

```bash
stack new my-project /path/to/identity-effectful.hsfiles \
  -p "author-name:John Doe" \
  -p "author-email:john@example.com" \
  -p "github-username:johndoe"
```

## Run

```bash
export DB_HOST=localhost
export DB_PORT=5432
export DB_USER=postgres
export DB_PASSWORD=postgres
export DB_DATABASE=my-project
export JWT_SECRET=your-secret-key

stack build
stack exec my-project-exe
```

## Test

```bash
stack test
```

## API

| Method | Path | Description | Auth |
|--------|------|-------------|------|
| POST | /api/register | Sign up | - |
| POST | /api/login | Log in | - |
| GET | /api/me | Get my profile | JWT |
| PUT | /api/me | Update profile | JWT |

Swagger UI: http://localhost:8080/swagger-ui
