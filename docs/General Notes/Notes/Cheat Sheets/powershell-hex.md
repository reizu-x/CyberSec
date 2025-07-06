# Powershell Hex Codes

## Failure Reason

- %%2305 : The specified user account has expired
- %%2309 : The specified account's password has expired
- %%2310 : Account currently disabled
- %%2311 : Account logon time restriction violation
- %%2312 : User not allowed to logon at this computer
- %%2313 : Unknown user name or bad password
- %%2304 : An Error occurred during Logon

## Status

- 0xC0000234 : Account locked out
- 0xC0000193 : Account expired 0xC0000133 : Clocks out of sync
- 0xC0000224 : Password change required
- 0xc000015b : User does not have logon right
- 0xc000006d : Logon failure
- 0xc000006e : Account restriction
- 0xc00002ee : An error occurred during logon
- 0xC0000071 : Password expired
- 0xC0000072 : Account disabled
- 0xC0000413 : Authentication firewall prohibits logon

## SubStatus

- 0xC0000234 : Account locked out
- 0xC0000193 : Account expired
- 0xC0000133 : Clocks out of sync
- 0xC0000224 : Password change required
- 0xc000015b : User does not have logon right
- 0xc000006d : Logon failure
- 0xc000006e : Account restriction
- 0xc00002ee : An error occurred during logon
- 0xC0000071 : Password expired
- 0xC0000072 : Account disabled
- 0xc000006a : Incorrect password
- 0xc0000064 : Account does not exist
- 0xC0000413 : Authentication firewall prohibits logon
- 0x1 : Client's entry in database has expired
- 0x2 : Server's entry in database has expired
- 0x3 : Requested protocol version # not supported
- 0x4 : Client's key encrypted in old master key
- 0x5 : Server's key encrypted in old master key
- 0x6 : Client not found in Kerberos database#Bad user name, or new computer/user account has not replicated to DC yet
- 0x7 : Server not found in Kerberos database# New computer account has not replicated yet or computer is pre-w2k
- 0x8 : Multiple principal entries in database
- 0x9 : The client or server has a null key# administrator should reset the password on the account
- 0xA : Ticket not eligible for postdating
- 0xB : Requested start time is later than end time
- 0xC : KDC policy rejects request# Workstation restriction
- 0xD : KDC cannot accommodate requested option
- 0xE : KDC has no support for encryption type
- 0xF : KDC has no support for checksum type
- 0x10 : KDC has no support for padata type
- 0x11 : KDC has no support for transited type
- 0x12 : Clients credentials have been revoked# Account disabled, expired, locked out, logon hours.
- 0x13 : Credentials for server have been revoked
- 0x14 : TGT has been revoked
- 0x15 : Client not yet valid - try again later
- 0x16 : Server not yet valid - try again later
- 0x17 : Password has expired# The user’s password has expired.
- 0x18 : Pre-authentication information was invalid# Usually means bad password
- 0x19 : Additional pre-authentication required*
- 0x1F : Integrity check on decrypted field failed
- 0x20 : Ticket expired#Frequently logged by computer accounts
- 0x21 : Ticket not yet valid
- 0x21 : Ticket not yet valid
- 0x22 : Request is a replay
- 0x23 : The ticket isn't for us
- 0x24 : Ticket and authenticator don't match
- 0x25 : Clock skew too great# Workstation’s clock too far out of sync with the DC’s
- 0x26 : Incorrect net address# IP address change?
- 0x27 : Protocol version mismatch
- 0x28 : Invalid msg type
- 0x29 : Message stream modified
- 0x2A : Message out of order
- 0x2C : Specified version of key is not available
- 0x2D : Service key not available
- 0x2E : Mutual authentication failed# may be a memory allocation failure
- 0x2F : Incorrect message direction
- 0x30 : Alternative authentication method required*
- 0x31 : Incorrect sequence number in message
- 0x32 : Inappropriate type of checksum in message
- 0x3C : Generic error (description in e-text)
- 0x3D : Field is too long for this implementation
