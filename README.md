# Expressões lambda
* Em programação funcional, expressão lambda corresponde a uma
função anônima de primeira classe.

```
public class Program {
    public static int compareProducts(Product p1, Product p2) {
    return p1.getPrice().compareTo(p2.getPrice());
}
  public static void main(String[] args) {
  
  (...)
  
  list.sort(Program::compareProducts);
  
  list.sort((p1, p2) -> p1.getPrice().compareTo(p2.getPrice()));
  (...)
```

# Interface funcional
* É uma interface que possui um único método abstrato. Suas
implementações serão tratadas como expressões lambda.

```
public class MyComparator implements Comparator<Product> {
  @Override
    public int compare(Product p1, Product p2) {
    return p1.getName().toUpperCase().compareTo(p2.getName().toUpperCase());
  }
}
```
```
public static void main(String[] args) {
    (...)
    list.sort(new MyComparator());
```

# Algumas outras interfaces funcionais comuns
* Predicate
  * Função que recebe um valor e retorna um boolean (ex:Filter)
  • https://docs.oracle.com/javase/8/docs/api/java/util/function/Predicate.html
* Function
  * Recebe e retorna um valor. (ex:Map)
  • https://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html
* Consumer
  * Recebe um valor e realiza algo com ele, porém ele não retorna nada. (ex: forEarch)
  • https://docs.oracle.com/javase/8/docs/api/java/util/function/Consumer.html
  • Nota: ao contrário das outras interfaces funcionais, no caso do Consumer, é
    esperado ele possa gerar efeitos colaterais
* Supplier 
   * Recebe nada, e retorna um valor. (ex: generate)
