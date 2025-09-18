# konkurens ea 2

ott hagytuk abba hogy nem determisztikus viselkedés
nem kéne hogy függjünk az ütemezéstől

## Ütemezési stratégiák
>
>### Run to completion
>>
>> fügvényhatárokig csinálja a dolgát sacc
>
> ### Preemptive
>>
>> igazságosabb

## Runnable interface
>
> futtatható a run() metódus
> egy thread-elt objektummal össze lehet kötni a lefutását
> leszármazásbeli előnyei vannak

## Névtelen szál is indítható

```java
(new Thread() { /**/ }).start()
```
