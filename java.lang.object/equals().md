### .equals()方法

```java
 /**
     * Indicates whether some other object is "equal to" this one.
     *
     * 译：指示其他某个对象是否“等于”这一个。
     *
     * <p>
     * The {@code equals} method implements an equivalence relation
     * on non-null object references:
     *
     * 译：{equals等式}方法在非null对象引用上实现等价关系：
     *
     * <ul>
     * <li>It is <i>reflexive</i>: for any non-null reference value
     *     {@code x}, {@code x.equals(x)} should return
     *     {@code true}.
     *
     * 译：它是自反的：对于任何非空引用值{code x}，
     * {@code x.equals（x）}应该返回{true}。
     *
     * <li>It is <i>symmetric</i>: for any non-null reference values
     *     {@code x} and {@code y}, {@code x.equals(y)}
     *     should return {@code true} if and only if
     *     {@code y.equals(x)} returns {@code true}.
     *
     * 译：它是对称的：对于任何非空引用值{code x}和{code y}，
     * {@code x.equals（y）}应该返回{true} 
     * 如果{@code y.equals（x）}返回{@code true}。
     *
     * <li>It is <i>transitive</i>: for any non-null reference values
     *     {@code x}, {@code y}, and {@code z}, if
     *     {@code x.equals(y)} returns {@code true} and
     *     {@code y.equals(z)} returns {@code true}, then
     *     {@code x.equals(z)} should return {@code true}.
     *
     * <li>It is <i>consistent</i>: for any non-null reference values
     *     {@code x} and {@code y}, multiple invocations of
     *     {@code x.equals(y)} consistently return {@code true}
     *     or consistently return {@code false}, provided no
     *     information used in {@code equals} comparisons on the
     *     objects is modified.
     *
     * 译：对于任何非空引用值{code x}和{code y}而言，
     * {@code x.equals（y）}的多次调用始终返回{@code true} 
     * 或者一致地返回{false}，只要修改了对象的{比较等于}比较中使用的信息。
     *
     * <li>For any non-null reference value {@code x},
     *     {@code x.equals(null)} should return {@code false}.
     * </ul>
     * <p>
     * The {@code equals} method for class {@code Object} implements
     * the most discriminating possible equivalence relation on objects;
     * that is, for any non-null reference values {@code x} and
     * {@code y}, this method returns {@code true} if and only
     * if {@code x} and {@code y} refer to the same object
     * ({@code x == y} has the value {@code true}).
     * <p>
     *
     * 译：对象类{@code Object}的{equals}方法实现对象上最可能的等价关系;
     * 也就是说，对于任何非空引用值{code x}和{code y}，
     * 当且仅当{code x}和{code y}引用同一对象时，此方法才返回{true} 
     *（{@code x == y}的值为{@code true}）。
     *
     * Note that it is generally necessary to override the {@code hashCode}
     * method whenever this method is overridden, so as to maintain the
     * general contract for the {@code hashCode} method, which states
     * that equal objects must have equal hash codes.
     *
     * 译：请注意，无论何时重写此方法，通常都必须重写hashCode方法，
     * 以便维护hashCode方法的常规协定，该方法声明相等对象必须具有相同的哈希码。
     *
     * @param   obj   the reference object with which to compare.
     * @return  {@code true} if this object is the same as the obj
     *          argument; {@code false} otherwise.
     * @see     #hashCode()
     * @see     java.util.HashMap
     */
    public boolean equals(Object obj) {
        return (this == obj);
    }
```

#### 总结：

1. x.equals(y) 需要x非空

2. equals() 只判断是否等价，== 判断是否为同一引用对象

3. 重写equals()方法需要重写hashCode() 该方法声明相等对象必须具有相同的哈希码。

4. > 1、如果两个对象相等，那么他们一定有相同的哈希值（hash code）。
   >
   > 2、如果两个对象的哈希值相等，那么这两个对象有可能相等也有可能不相等。（需要再通过equals来判断）

