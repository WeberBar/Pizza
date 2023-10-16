# Pizza

### Crie um relatório com todas as pizzas e os pizzaiolos aptos a produzi-las
``` sql
-- Seleciona o sabor da pizza e concatena os nomes dos pizzaiolos que a preparam.
select pizza.sabor as Sabor, group_concat(pizzaiolo.nome) as Pizzaiolos
-- Faz um join entre as tabelas pizza, pizza_has_pizzaiolo e pizzaiolo.
from pizza
join pizza_has_pizzaiolo
 on pizza.id = pizza_has_pizzaiolo.Pizza_id
 join pizzaiolo on pizzaiolo.id = pizza_has_pizzaiolo.Pizzaiolo_id
-- Agrupa os dados pelo sabor da pizza.
group by pizza.sabor;

´´´

![pizzaria1](pizza_e_pizzaiolos.png)
