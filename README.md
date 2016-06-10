# java8streams

#Intermediate Operations
###Stream
Stream<T> filter(Predicate<? super T> predicate)
###Map
<R> Stream<R> map(Function<? super T,? extends R> mapper)
###mapToInt
IntStream mapToInt(ToIntFunction<? super T> mapper)
###mapToLong
LongStream mapToLong(ToLongFunction<? super T> mapper)
###mapToDouble
DoubleStream mapToDouble(ToDoubleFunction<? super T> mapper)
###flatMap
<R> Stream<R> flatMap(Function<? super T,? extends Stream<? extends R>> mapper)
###flatMapToInt
IntStream flatMapToInt(Function<? super T,? extends IntStream> mapper)
###flatMapToLong
LongStream flatMapToLong(Function<? super T,? extends LongStream> mapper)
###flatMapToDouble
DoubleStream flatMapToDouble(Function<? super T,? extends DoubleStream> mapper)
###peek
Stream<T> peek(Consumer<? super T> action)

#Terminal Operations
###forEach
void forEach(Consumer<? super T> action)
###forEachOrdered
void forEachOrdered(Consumer<? super T> action)
###toArray
Object[] toArray()
###toArray
<A> A[] toArray(IntFunction<A[]> generator)
###reduce
T reduce(T identity,
         BinaryOperator<T> accumulator)
###reduce
Optional<T> reduce(BinaryOperator<T> accumulator)
###reduce
<U> U reduce(U identity,
             BiFunction<U,? super T,U> accumulator,
             BinaryOperator<U> combiner)
###collect
<R> R collect(Supplier<R> supplier,
              BiConsumer<R,? super T> accumulator,
              BiConsumer<R,R> combiner)
###collect
<R,A> R collect(Collector<? super T,A,R> collector)
###min
Optional<T> min(Comparator<? super T> comparator)
###max
Optional<T> max(Comparator<? super T> comparator)
###count
long count()
