## Define emits using type paramater
```ts
    const emits = defineEmits<{
      (e: 'addItem', stock: Item): void
      (e: 'updateItem', stock: Item): void
      (e: 'cancel'): void
    }>()
```

## use type as props on vue ts
```ts
    const props = defineProps<{
        productList: {
            type: Object as PropType<cartProduct[]>,
            required: true
        }
    }>
```
