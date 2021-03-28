English / [中文](./README_CN.md) 

# Evidence Demo

An multi-chain suitable Evidece Demo which supporting Highway Consortium Blockchain and FISCO BCOS Consortium Blockchain now.

> Try the demo online!
>
> https://elixir.leeduckgo.com/
>
> Admin Account: 
>
> Account Name:  highway
>
> Password:  leeduckgo

## 1. Install Erlang and Elixir

Install Erlang：

> https://www.erlang-solutions.com/downloads/

Install Elixir: 

> https://elixir-lang.org/install.html

Tips -- Cheatsheet for how to install on Ubuntu: 

> 1. Install Erlang
>
>    Download：
>
>    ```
>    wget http://www.erlang.org/download/[version].tar.gz
>    ```
>
>    Unzip：
>
>    ```
>    tar -zxf otp_src_20.2.tar.gz
>    ```
>
>    Install the thing that needed: 
>
>    ```
>    cd otp_src_20.2
>    sudo apt-get install openssl
>    sudo apt-get install libssl-dev
>    sudo apt-get install libncurses5-dev libncursesw5-dev
>    apt install libwxgtk3.0-dev
>    apt install unixodbc
>    apt install unixodbc-dev
>    ```
>
>    Configure:
>
>    ```
>    ./configure
>    ```
>
>    Compile:
>
>    ```
>    sudo make&&make install
>    ```
>
>    Check it:
>
>    ```
>    erl
>    ```
>
> 2. Install Elixir
>
>    Add Erlang Solutions repository: 
>
>    ```
>    wget https://packages.erlang-solutions.com/erlang-solutions_2.0_all.deb && sudo dpkg -i erlang-solutions_2.0_all.deb
>    sudo apt-get update
>    ```
>
>    Install Elixir:
>
>    ```
>     sudo apt-get install elixir
>    ```

## 2 Install Postgres

Guide: 

> https://www.cnblogs.com/z-sm/p/5644165.html

## 3 Init

1. Cd to folder:

```
cd evidence_demo
```

2. Init

```elixir
mix setup
```

3. Copy `priv/repo/seeds.exs.template` to `priv/repo/seeds.exs`

```
cp priv/repo/seeds.exs.template priv/repo/seeds.exs
```

4. Modify the params necessary, including `ip` and `port`, user info and contract info.

5. Run the script: 

```elixir
mix run priv/repo/seeds.exs
```

## 4 Run

The default port is 4000:

```
iex -S mix phx.server
```

Default Admin Account：leeduckgo 

Default Admin Password：jbjhhzstsl