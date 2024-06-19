# [Get] Network

```
https://api.cryptoscan.pro/v1/networks/{networkId}
```

## Request

```
{
  /**
    * Coin name, ticker or contract
    */
  coin?: string;
}
```

## Response

```
{
  id: number;
  name: string;
  fullName: string;
  aliases: string[];
  /**
    * Centralized exchanges statuses, includes with `coin` param
    */
  exchanges?: {
    [exchangeName]: {
      isEnabled: boolean;
      enabledAt: Date;
      disabledAt: Date;
    }
  }
}
```

## Example

```
curl -X GET "https://api.cryptoscan.pro/v1/networks"
```
