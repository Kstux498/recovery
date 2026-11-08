# Recovery bundle

Encrypted backup of keys, configuration and documents. Without the owner's passphrase these files are useless.

## How to open it (any computer)

1. Download from the **latest release** (right side of this page, or `/releases/latest`):
   `identity.age`, `recovery-keys.tar.gz.age`, and for documents all `recovery-documents.tar.gz.age.part-*` files.
2. Download **age** for your system from https://github.com/FiloSottile/age/releases/latest and unpack it.
3. In a terminal, in the download folder:

   Linux or Mac:

       age -d -i identity.age recovery-keys.tar.gz.age | tar xz

   Windows (PowerShell or cmd):

       age.exe -d -i identity.age -o keys.tar.gz recovery-keys.tar.gz.age
       tar xzf keys.tar.gz

   age asks for the passphrase (six words, separated by spaces, all lowercase).
4. Open `recovery-keys/START-HERE.md` and follow it.
