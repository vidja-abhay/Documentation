# JSON Web Token (JWT)

## Table of Contents
1. [What is JWT?](#what-is-jwt)
2. [Structure of JWT](#structure-of-jwt)
3. [How to Create a JWT](#how-to-create-a-jwt)
4. [How to Validate JWT](#how-to-validate-jwt)
5. [How JWT Works](#how-jwt-works)
6. [Why We Use JWT](#why-we-use-jwt)

## What is JWT?

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.

## Structure of JWT

A JWT consists of three parts separated by dots (.):

1. Header
2. Payload
3. Signature 

### Header
The header typically consists of two parts: the type of the token (JWT) and the signing algorithm being used (e.g., HMAC SHA256 or RSA).

### Payload
The payload contains claims. Claims are statements about an entity (typically, the user) and additional data.

### Signature
To create the signature part, you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

## How to Create a JWT

To create a JWT:

1. Define the header and payload
2. Encode the header and payload using Base64Url encoding
3. Create a signature using a secret key and the specified algorithm
4. Concatenate the encoded header, payload, and signature with dots

Example using Node.js and the jsonwebtoken library:

bash
const jwt = require('jsonwebtoken');
const secretKey = 'your-secret-key';

const payload = {
  userId: 123,
  username: 'johndoe'
};

const token = jwt.sign(payload, secretKey, { expiresIn: '1h' });

## How to Validate JWT

- Split the token into its three parts
- Decode the header and payload
- Verify the signature using the secret key and the algorithm specified in the header
- Check if the token has expired
- Verify any additional claims as required by your application

bash
const jwt = require('jsonwebtoken');
const secretKey = 'your-secret-key';

function verifyToken(token) {
  try {
    const decoded = jwt.verify(token, secretKey);
    return decoded;
  } catch (err) {
    console.error('Invalid token:', err.message);
    return null;
  }
}


## How JWT Works

1. The client sends credentials to the server
2. The server verifies the credentials and generates a JWT
3. The server sends the JWT back to the client
4. The client stores the JWT (usually in local storage)
5. The client includes the JWT in the header of subsequent requests
6. The server validates the JWT for each request and grants access to resources if valid

## Why We Use JWT

**1. Stateless authentication**: Servers don't need to store session information.

**2. Scalability**: Easy to scale across different domains and services.

**3. Security**: Signed tokens ensure data hasn't been tampered with.

**4. Efficiency**: Compact size makes it easy to transmit in HTTP headers.

**5. Flexibility**: Can include custom claims to suit specific use cases.

**6.Cross-domain / CORS**: Easy to use across different domains