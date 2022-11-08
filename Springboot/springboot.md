# Notaciones

Las anotaciones proveen informacion **suplementaria** sobre un programa. No es parte de lo que se desarrolla. No tiene un impacto directo en la operación del codigo que anotan.

## Notaciones Core Spring Framework

**@Required**: Aplica al metodo **bean** setter. Indica que el bean debe completarse en el momento de la configuración con la propiedad requerida; de lo contrario arroja una expepción **BeanInitilizationException**.

### Ejemplo

```java
public class Machine   
{  
private Integer cost;  
@Required  
public void setCost(Integer cost)   
{  
this.cost = cost;  
}  
public Integer getCost()   
{  
return cost;  
}     
}  
```

Para más información ir a la [documentación](https://www.javatpoint.com/spring-boot-annotations)