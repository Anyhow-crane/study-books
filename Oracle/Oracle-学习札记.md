#### 导入 oracle 命令

```shell
imp ahdx_codemix/ahdx_codemix117148 file=/home/oracle/rr_asset_entity_ahw.dmp full=y grants=n
```

> 不用写SID,如:用户/密码@SID

#### Oracle rac 双库 jdbc 连接语句

```
jdbc.url=jdbc:oracle:thin:@(description=(address_list=(address=(host=137.64.37.156)(protocol=tcp)(port=1521))(address=(host=137.64.37.157)(protocol=tcp)(port=1521))(load_balance=yes)(failover=on))(connect_data=(service_name=SXDXITSP)))
```

