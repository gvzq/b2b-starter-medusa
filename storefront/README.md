# Medusa B2B Commerce Storefront

This is the storefront for the Medusa B2B Commerce Starter. Follow these steps to get started.

## Setup Instructions

### Prerequisites

- Backend server running at http://localhost:9000
- Admin credentials (default: admin@test.com / supersecret)

### Environment Setup

Clone the `.env.template` file:
```bash
cp .env.template .env
```

Configure the publishable API key:

- Log in to the Medusa Admin at http://localhost:9000/app
- Navigate to Settings → API Keys → Publishable API Keys
- You should see a "Webshop" key already created during seeding
- Click on the key to view its details
- Copy the token value
- Add it to your `.env` file:

```env
NEXT_PUBLIC_MEDUSA_PUBLISHABLE_KEY=pk_xxxx...
```

Start the development server:

```bash
yarn dev
```

1. Access the storefront at [http://localhost:8000](http://localhost:8000)

## Troubleshooting

If you see errors like "A valid publishable key is required to proceed with the request", make sure:

1. You've added the correct publishable key to your `.env` file
2. The key is associated with the appropriate sales channels
3. The backend server is running

## Additional Resources

For more information, refer to the main [B2B Commerce Starter documentation](https://github.com/medusajs/b2b-starter-medusa/wiki).
