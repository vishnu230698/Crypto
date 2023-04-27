 # generates symmetric key
openssl rand -hex 16 > Saketh_key.txt

# to create encrypted file using key 
openssl enc -aes-256-cbc -in Saketh_msg.txt -out Saketh_encrypted.txt -k file:Saketh_key.txt
# command to decrypt the file
openssl enc -d -aes-256-cbc -in Saketh_encrypted.txt -out Saketh_decrypted.txt -k file:Saketh_key.txt