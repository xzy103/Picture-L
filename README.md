# API参考

---
[TOC]
## AccountAPI

- 获取币种列表
```python
get_currencies(self)
```
- 钱包账户信息
```python
get_wallet(self)
```
- 单一币种账户信息
```python
get_currency(self, symbol)
```
- 提币
```python
coin_withdraw(self, currency, amount, destination, to_address, trade_pwd, fee)
```
- 提币手续费
```python
get_coin_fee(self, symbol='')
```
- 查询最近所有币种的提币记录
```python
get_coins_withdraw_record(self)
```
- 查询单个币种提币记录
```python
get_coin_withdraw_record(self, symbol)
```
- 账单流水查询
```python
get_ledger_record(self, froms, to, limit, currency='', ctype='')
```

- 获取充值地址
```python
get_top_up_address(self, symbol)
```
- 获取所有币种充值记录
```python
get_top_up_records(self)
```
- 获取单个币种充值记录
```python
get_top_up_record(self, symbol)
```
- 资金划转
```python
coin_transfer(self, currency, amount, account_from, account_to, sub_account='', instrument_id='')
```

## FutureAPI
- 合约持仓信息
```python
get_position(self)
```
- 单个合约持仓信息
```python
get_specific_position(self, instrument_id)
```
- 合约账户信息
```python
get_accounts(self)
```
- 某个币种合约账户信息
```python
get_coin_account(self, symbol)
```
- 获取合约币种杠杆倍数
```python
get_leverage(self, symbol)
```
- 设定合约币种杠杆倍数
```python
def set_leverage(self, symbol, instrument_id='', direction='', leverage=10)
```
- 账单流水查询
```python
get_ledger(self, symbol)
```
- 平掉所有仓位
```python
revoke_position(self, position_data)
```
- 下单
```python
take_order(self, client_oid, instrument_id, otype, price, size, match_price, leverage):
```
- 批量下单
```python
take_orders(self, instrument_id, order_data, leverage)
```
- 撤销指定订单
```python
revoke_order(self, order_id)
```
- 批量撤销订单
```python
revoke_orders(self, instrument_id)
```
- 获取订单列表
```python
get_order_list(self, status, froms, to, limit, instrument_id='')
```

- 获取订单信息
```python
get_order_info(self, order_id, instrument_id)
```
- 获取成交明细
```python
get_fills(self, order_id, instrument_id, froms, to, limit)
```

- 获取合约信息
```python
get_products(self)
```
- 获取深度数据
```python
get_depth(self, instrument_id, size)
```
- 获取全部ticker信息
```python
get_ticker(self)
```
- 获取某个ticker信息
```python
get_specific_ticker(self, instrument_id)
```
- 获取成交数据(新版)
```python
get_trades(self, instrument_id, froms, to, limit):
```

- 获取K线数据
```python
get_kline(self, instrument_id, granularity, start='', end='')
```
- 获取指数信息
```python
get_index(self, instrument_id)
```
- 获取法币汇率
```python
get_rate(self)
```
- 获取预估交割价
```python
get_estimated_price(self, instrument_id)
```
- 获取平台总持仓量
```python
get_holds(self, instrument_id):
```
- 获取当前限价
```python
get_limit(self, instrument_id)
```
- 获取爆仓单
```python
get_liquidation(self, instrument_id)
```

* 获取合约挂单冻结数量

```python
get_holds_amount(self, instrument_id)
```
