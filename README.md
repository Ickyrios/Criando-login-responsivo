# Tutorial login responsivo da  Giovanna moeller, @girl coding com algumas modificações

Quando apliquei as modificações, ao abrir o index.html no windows, alguns elementos ficava fora de lugar,
a solução foi criar um ::before e mover algumas configurações de lugar, 
e ir modificando tudo novamente, como foi o caso da div.loading no CSS


## Correção de erro no CSS

- antes


```css
.loading{
 position: relative;
 display: flex;
 border: 8px solid rgba(0, 0, 0, 0.1);
 border-right-color: #12dfbc;
 border-left-color: #12dfbc;
 border-top-color: #12dfbc;
 border-bottom-color: #0fbb9e;

 height: 26px;
 width: 26px;
 bottom: 60px;
 right: 250px;
 border-radius: 50%;
```

## Solução do erro no CSS
- depois 

```css
.loading {
   position: relative;
   display: flex;
   width: 100%;
  
}

.loading::before {
   content: '';
   position: absolute;
   border: 8px solid rgba(0, 0, 0, 0.1);
   border-right-color: #12dfbc;
   border-left-color: #12dfbc;
   border-top-color: #12dfbc;
   border-bottom-color: #0fbb9e;
 
   height: 8px;
   width: 8px;
   bottom: 35px;
   right: 0;
   border-radius: 50%;
}
```