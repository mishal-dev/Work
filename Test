from pgpy.constants import CompressionAlgorithm, SymmetricKeyAlgorithm
from pgpy import PGPMessage, PGPKey

# Load your private key
key = PGPKey.from_file('your_private_key.asc')

# Create a PGP message
message = PGPMessage.new('your_message', compress=CompressionAlgorithm.Uncompressed)

# Encrypt the message with MDC enabled
encrypted_message = key.encrypt(message, cipher=SymmetricKeyAlgorithm.AES256, mdc=True)

# Decrypt the encrypted message
decrypted_message = key.decrypt(encrypted_message)

print(decrypted_message.message)
