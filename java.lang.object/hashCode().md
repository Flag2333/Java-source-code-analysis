### .hashCode()方法
```java
/**
     * Returns a hash code value for the object. This method is
     * supported for the benefit of hash tables such as those provided by
     * {@link java.util.HashMap}.
     *
     * 译：返回对象的哈希码值。 
     * 为了散列表的好处而支持此方法，例如由{@link java.util.HashMap}提供的散列表。
     *
     * <p>
     * The general contract of {@code hashCode} is:
     * <ul>
     *
     * 译：{@code hashCode}的一般合约是：
     *
     * <li>Whenever it is invoked on the same object more than once during
     *     an execution of a Java application, the {@code hashCode} method
     *     must consistently return the same integer, provided no information
     *     used in {@code equals} comparisons on the object is modified.
     *     This integer need not remain consistent from one execution of an
     *     application to another execution of the same application.
     *
     * 译：只要在Java应用程序的执行过程中多次调用同一对象时，
     * {@code hashCode}方法必须始终返回相同的整数，
     * 只要修改了在对象上{@code equals}比较中使用的信息即可。
     * 该整数不需要从应用程序的一次执行到同一应用程序的另一次执行保持一致。
     *
     * <li>If two objects are equal according to the {@code equals(Object)}
     *     method, then calling the {@code hashCode} method on each of
     *     the two objects must produce the same integer result.
     *
     * 译：如果两个对象根据equals方法相等，
     * 则在两个对象的每一个对象上调用hashCode方法必须产生相同的整数结果。
     *
     * <li>It is <em>not</em> required that if two objects are unequal
     *     according to the {@link java.lang.Object#equals(java.lang.Object)}
     *     method, then calling the {@code hashCode} method on each of the
     *     two objects must produce distinct integer results.  However, the
     *     programmer should be aware that producing distinct integer results
     *     for unequal objects may improve the performance of hash tables.
     * </ul>
     *
     * 译：根据{@link java.lang.Object＃equals（java.lang.Object）}方法，
     * 如果两个对象不相等，则不需要<em> em </ em>，然后调用{@code hashCode}方法 
     * 两个对象中的每一个都必须产生不同的整数结果。 
     * 但是，程序员应该意识到，为不相等的对象生成不同的整数结果可能会提高散列表的性能。
     * <p>
     * As much as is reasonably practical, the hashCode method defined by
     * class {@code Object} does return distinct integers for distinct
     * objects. (This is typically implemented by converting the internal
     * address of the object into an integer, but this implementation
     * technique is not required by the
     * Java&trade; programming language.)
     *
     * 译：尽可能合理实用，类{@CodeObject}定义的hashCode方法确实为不同的对象返回不同的整数。 
     *（这通常通过将对象的内部地址转换为整数来实现，但这种实现技术并不是Java编程语言所要求的。）
     *
     * @return  a hash code value for this object.
     * @see     java.lang.Object#equals(java.lang.Object)
     * @see     java.lang.System#identityHashCode
     */
    public native int hashCode();
```

#### 总结：

1. hashCode的生命周期是应用程序开始到应用程序结束，一个生命周期内，多次调用同一对象hashCode一定相同，重启应用程序后不一定相同。
2. .equals()方法等于true，返回的hashCode相同，为false，不同的两个对象一定返回不同的两个整数。