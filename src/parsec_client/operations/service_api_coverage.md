# Parsec Operations Coverage

These tables define the current level of coverage in Parsec for the operations and their parameters.
Only the operations [specified](README.md) and that have a dedicated page are put in the following
table.

Not all parameters (key types, algorithms) of the operation might be supported. See the following
sections for details.

| Operation                                         | Core provider | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|---------------------------------------------------|---------------|----------------------|------------------|------------------|
| [Ping](ping.md)                                   | ✅           | ❌                  | ❌              | ❌              |
| [ListProviders](list_providers.md)                | ✅           | ❌                  | ❌              | ❌              |
| [ListOpcodes](list_opcodes.md)                    | ✅           | ❌                  | ❌              | ❌              |
| [ListAuthenticators](list_authenticators.md)      | ✅           | ❌                  | ❌              | ❌              |
| [PsaImportKey](psa_import_key.md)                 | ❌           | ✅                  | ✅              | ✅              |
| [PsaGenerateKey](psa_generate_key.md)             | ❌           | ✅                  | ✅              | ✅              |
| [PsaDestroyKey](psa_destroy_key.md)               | ❌           | ✅                  | ✅              | ✅              |
| [PsaExportKey](psa_export_key.md)                 | ❌           | ✅                  | ❌              | ❌              |
| [PsaExportPublicKey](psa_export_public_key.md)    | ❌           | ✅                  | ✅              | ✅              |
| [PsaHashCompute](psa_hash_compute.md)             | ❌           | ✅                  | ❌              | ❌              |
| [PsaHashCompare](psa_hash_compare.md)             | ❌           | ✅                  | ❌              | ❌              |
| [PsaMacCompute](psa_mac_compute.md)               | ❌           | ❌                  | ❌              | ❌              |
| [PsaMacVerify](psa_mac_verify.md)                 | ❌           | ❌                  | ❌              | ❌              |
| [PsaCipherEncrypt](psa_cipher_encrypt.md)         | ❌           | ❌                  | ❌              | ❌              |
| [PsaCipherDecrypt](psa_cipher_decrypt.md)         | ❌           | ❌                  | ❌              | ❌              |
| [PsaAeadEncrypt](psa_aead_encrypt.md)             | ❌           | ✅                  | ❌              | ❌              |
| [PsaAeadDecrypt](psa_aead_decrypt.md)             | ❌           | ✅                  | ❌              | ❌              |
| [PsaSignMessage](psa_sign_message.md)             | ❌           | ❌                  | ❌              | ❌              |
| [PsaVerifyMessage](psa_verify_message.md)         | ❌           | ❌                  | ❌              | ❌              |
| [PsaSignHash](psa_sign_hash.md)                   | ❌           | ✅                  | ✅              | ✅              |
| [PsaVerifyHash](psa_verify_hash.md)               | ❌           | ✅                  | ✅              | ✅              |
| [PsaAsymmetricEncrypt](psa_asymmetric_encrypt.md) | ❌           | ✅                  | ❌              | ❌              |
| [PsaAsymmetricDecrypt](psa_asymmetric_decrypt.md) | ❌           | ✅                  | ❌              | ❌              |
| [PsaRawKeyAgreement](psa_raw_key_agreement.md)    | ❌           | ✅                  | ❌              | ❌              |
| [PsaGenerateRandom](psa_generate_random.md)       | ❌           | ✅                  | ❌              | ❌              |

### Key types support

This table describe if the following [key types](psa_key_attributes.md#keytype-type) are supported
for key management operations.

| Key type     | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|--------------|----------------------|------------------|------------------|
| RawData      | ✅                  | ❌              | ❌              |
| Hmac         | ❌                  | ❌              | ❌              |
| Derive       | ❌                  | ❌              | ❌              |
| Aes          | ✅                  | ❌              | ❌              |
| Des          | ❌                  | ❌              | ❌              |
| Camellia     | ✅                  | ❌              | ❌              |
| Arc4         | ❌                  | ❌              | ❌              |
| Chacha20     | ✅                  | ❌              | ❌              |
| RsaPublicKey | ✅                  | ✅              | ✅              |
| RsaKeyPair   | ✅                  | ✅              | ✅              |
| EccKeyPair   | ✅                  | ❌              | ✅              |
| EccPublicKey | ✅                  | ❌              | ✅              |
| DhKeyPair    | ✅                  | ❌              | ❌              |
| DhPublicKey  | ✅                  | ❌              | ❌              |

### Algorithm support

These tables describe if the following [algorithms](psa_algorithm.md) are supported in all
cryptographic operations they could be used in.

#### Hash algorithms

| Algorithm   | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|-------------|----------------------|------------------|------------------|
| MD2         | ✅                  | ❌              | ❌              |
| MD4         | ✅                  | ❌              | ❌              |
| MD5         | ✅                  | ❌              | ❌              |
| RIPEMD-160  | ✅                  | ❌              | ❌              |
| SHA-1       | ✅                  | ❌              | ✅              |
| SHA-224     | ✅                  | ❌              | ❌              |
| SHA-256     | ✅                  | ✅              | ✅              |
| SHA-384     | ✅                  | ❌              | ✅              |
| SHA-512     | ✅                  | ❌              | ✅              |
| SHA-512/224 | ✅                  | ❌              | ❌              |
| SHA-512/256 | ✅                  | ❌              | ❌              |
| SHA3-224    | ✅                  | ❌              | ❌              |
| SHA3-256    | ✅                  | ❌              | ✅              |
| SHA3-384    | ✅                  | ❌              | ✅              |
| SHA3-512    | ✅                  | ❌              | ✅              |

### MAC algorithms

| Algorithm | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|-----------|----------------------|------------------|------------------|
| HMAC      | ❌                  | ❌              | ❌              |
| CBC-MAC   | ❌                  | ❌              | ❌              |
| CMAC      | ❌                  | ❌              | ❌              |

### Cipher algorithms

| Algorithm                | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|--------------------------|----------------------|------------------|------------------|
| Stream Cipher            | ❌                  | ❌              | ❌              |
| CTR                      | ❌                  | ❌              | ❌              |
| CFB                      | ❌                  | ❌              | ❌              |
| OFB                      | ❌                  | ❌              | ❌              |
| XTS                      | ❌                  | ❌              | ❌              |
| ECB with no padding      | ❌                  | ❌              | ❌              |
| CBC with no padding      | ❌                  | ❌              | ❌              |
| CBCP with PKCS#7 padding | ❌                  | ❌              | ❌              |

#### AEAD algorithms

| Algorithm         | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|-------------------|----------------------|------------------|------------------|
| CCM               | ✅                  | ❌              | ❌              |
| GCM               | ✅                  | ❌              | ❌              |
| ChaCha20-Poly1305 | ✅                  | ❌              | ❌              |

#### Asymmetric signature algorithms

| Algorithm                                  | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|--------------------------------------------|----------------------|------------------|------------------|
| RSA PKCS#1 v1.5 signature with hashing     | ✅                  | ✅              | ✅              |
| Raw PKCS#1 v1.5 signature                  | ❌                  | ❌              | ❌              |
| RSA PSS signature with hashing             | ❌                  | ❌              | ❌              |
| ECDSA signature with hashing               | ❌                  | ❌              | ✅              |
| ECDSA signature without hashing            | ❌                  | ❌              | ❌              |
| Deterministic ECDSA signature with hashing | ❌                  | ❌              | ❌              |

#### Asymmetric encryption algorithms

| Algorithm                  | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|----------------------------|----------------------|------------------|------------------|
| RSA PKCS#1 v1.5 encryption | ✅                  | ❌              | ❌              |
| RSA OAEP encryption        | ✅                  | ❌              | ❌              |

#### Key agreement algorithms

| Algorithm | Mbed Crypto provider | PKCS 11 provider | TPM 2.0 provider |
|-----------|----------------------|------------------|------------------|
| FFDH      | ✅                  | ❌              | ❌              |
| ECDH      | ✅                  | ❌              | ❌              |

## Increasing PSA API coverage

You can help increase the coverage of the PSA Crypto API! See
[here](../../contributing/adding_new_operation_how_to.md) on how you can contribute.

*Copyright 2020 Contributors to the Parsec project.*