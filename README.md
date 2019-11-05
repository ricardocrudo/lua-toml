# lua-toml-redis

This project is a fork of [lua-toml](https://github.com/jonstoler/lua-toml) which was modified to
read a toml file and export the contents to [redis](https://redis.io/).

# Usage

	redis-cli --eval toml-redis.lua , "`cat /path/to/file.toml`"
    redis-cli --eval toml-redis.lua , "`cat /path/to/file.toml`" "mykey"

In the first example a hash named **settings** is created and the contents of the TOML file are
created as fields of that hash. In the second command above, the behavior is the same but the
contents are added to **mykey** instead.

# License

lua-toml is licensed under [MIT](https://opensource.org/licenses/MIT) and written by Jonathan
Stoler.

lua-toml-redis is licensed under [MIT](https://opensource.org/licenses/MIT).
