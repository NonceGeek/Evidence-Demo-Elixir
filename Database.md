# 数据库结构设计

## Chain

name string
min_height integer
is_enabled boolean
adapter Enum
config map
height_now integer

## Block
block_height integer
block_hash string
timestamp big_uint/decimal
---
chain_id integer

## Contract
addr string
creater string
init_params map
description stirng
---
chain_id integer

## Transaction

tx_hash string
from string
to string 
_value big_uint/decimal
---
block_id integer
contract_id integer

## Event

address string
log_index integer
topics  list
data string
block_height integer
---
tx_id integer