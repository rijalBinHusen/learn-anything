## merubah seluruh interface order menjadi optional // id?, date? dst
```ts
interface Order {
  id: string
  date_order: string
  id_group: string
  is_group: boolean
  id_product: string
  name_of_customer: string
  sent: string
  title: string
  total_balance: number
}

//Kode dibawah akan merubah seluruh interface order menjadi optional // id?, date? dst
type OrderUpdate = {
  [K in keyof Order]?:  Order[K];
}

```


## set variable type sebagai setTimeout
```ts
let timer: ReturnType<typeof setTimeout>;
```

