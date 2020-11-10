# ASaltHash

Funciona em Sistemas Linux
Requer Openssl instalado

ASaltHash é uma ferramenta para criar Hashs com Salt apartir de senhas, no padrão do Linux...

Documentação:
https://www.man7.org/linux/man-pages/man3/crypt.3.html

"
Features in glibc
       The glibc version of this function supports additional encryption
       algorithms.

       If salt is a character string starting with the characters "$id$"
       followed by a string optionally terminated by "$", then the result
       has the form:

              $id$salt$encrypted

       id identifies the encryption method used instead of DES and this then
       determines how the rest of the password string is interpreted.  The
       following values of id are supported:

              ID  | Method
              ─────────────────────────────────────────────────────────
              1   | MD5
              2a  | Blowfish (not in mainline glibc; added in some
                  | Linux distributions)
              5   | SHA-256 (since glibc 2.7)
              6   | SHA-512 (since glibc 2.7)

       Thus, $5$salt$encrypted and $6$salt$encrypted contain the password
       encrypted with, respectively, functions based on SHA-256 and SHA-512.

       "salt" stands for the up to 16 characters following "$id$" in the
       salt.  The "encrypted" part of the password string is the actual
       computed password.  The size of this string is fixed:

       MD5     | 22 characters
       SHA-256 | 43 characters
       SHA-512 | 86 characters

       The characters in "salt" and "encrypted" are drawn from the set
       [a-zA-Z0-9./].  In the MD5 and SHA implementations the entire key is
       significant (instead of only the first 8 bytes in DES).
       
  model:     $id$salt$encrypted


"


USO:

┌─[root@parrot]─[/home]
└──╼ #./ASaltHash.sh

		    _    ____          _  _    _   _              _
		   / \  / ___|   __ _ | || |_ | | | |  __ _  ___ | |__
		  //_\\ \___ \  / _  || || __|| |_| | / _  |/ __||  _ \
		 / ___ \ ___) || (_| || || |_ |  _  || (_| |\__ \| | | |
		/_/   \_\____/  \__,_||_| \__||_| |_| \__,_||___/|_| |_|
            		     Version 1.1    Author @BlackCyber
			     https://github.com/BlackCyber21/


                      Modo de uso: ./ASaltHash.sh id salt senha

┌─[root@parrot]─[/home]
└──╼ #./ASaltHash.sh --help

		    _    ____          _  _    _   _              _
		   / \  / ___|   __ _ | || |_ | | | |  __ _  ___ | |__
		  //_\\ \___ \  / _  || || __|| |_| | / _  |/ __||  _ \
		 / ___ \ ___) || (_| || || |_ |  _  || (_| |\__ \| | | |
		/_/   \_\____/  \__,_||_| \__||_| |_| \__,_||___/|_| |_|
            		     Version 1.1    Author @BlackCyber
			     https://github.com/BlackCyber21/


                  Modo de uso: ./ASaltHash.sh 6 r06hSt2YoUlJ5Lui 12345678

┌─[root@parrot]─[/home]
└──╼ #./ASaltHash.sh 6 r06hSt2YoUlJ5Lui 12345678

		    _    ____          _  _    _   _              _
		   / \  / ___|   __ _ | || |_ | | | |  __ _  ___ | |__
		  //_\\ \___ \  / _  || || __|| |_| | / _  |/ __||  _ \
		 / ___ \ ___) || (_| || || |_ |  _  || (_| |\__ \| | | |
		/_/   \_\____/  \__,_||_| \__||_| |_| \__,_||___/|_| |_|
            		     Version 1.1    Author @BlackCyber
			     https://github.com/BlackCyber21/


$6$r06hSt2YoUlJ5Lui$uTLTDFbAI1yIB9CBr6FRPCoDQSEzkO4BFC5sfuZwbi.qBN/vzNadisf6Y6Y2UUTzjg0nJr7w3RY2AXSU3XP2T1

