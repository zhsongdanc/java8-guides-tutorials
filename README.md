# Java 8 Guides and Tutorials

**Java 8**  changed the way that we think and code. Here you will see a **lot of articles and tutorials**
about Java 8, how to use its awesome features and how to get your life easier! Enjoy!

- [Twitter](https://twitter.com/_alex_gama)
- [GitHub](https://github.com/alexandregama)
- [Linkedin](https://www.linkedin.com/in/alexandregama/)
- [Instagram](https://www.instagram.com/_alex_gama)
- [Youtube](https://www.youtube.com/channel/UCn09BXJXOCPLARsqNvxEFuw)

Running out of time?
Go straight to what you want :)

- [Java 8 - Lambda Expression](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/lambda/LambdaExpressionTest.java)
- [Java 8 - Default Methods](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/defaultmethod/DefaultMethodTest.java)
- [Java 8 - Functions](https://github.com/alexandregama/java8-guides-tutorials/tree/master/src/test/java/functions)
- [Java 8 - Stream Count](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/streams/StreamWithCountTest.java)
- [Java 8 - Stream with Filter](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/streams/StreamWithFilterTest.java)
- [Java 8 - Stream with Map](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/streams/StreamWithMapTest.java)
- [Java 8 - Stream with Sorted](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/streams/StreamWithSortedTest.java)
- [Java 8 - Stream with Match](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/streams/StreamWithMatchTest.java)
- [Java 8 - Stream Reduce](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/streams/StreamReduceTest.java)
- [Java 8 - Stream Consumer](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/consumer/ConsumerFunctionalInterfaceTest.java)
- [Java 8 - Predicate](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/predicate/PredicateFunctionalInterfaceTest.java)
- [Java 8 - Comparator](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/comparator/ComparatorFunctionalInterfaceTest.java)
- [Java 8 - Suppliers](https://github.com/alexandregama/java8-guides-tutorials/blob/master/src/test/java/suppliers/SupplierFunctionalInterfaceTest.java)



Stream原理初探
DISTINCT(StreamOpFlag): 
	bitPosition: 0
	set: 01 << 0  = 01
	clear: 10 << 0 = 10
	preserve: 11 << 0 = 11
	maskTable: <StreamOpFlag.Type.SPLITERATOR, 01>
				<StreamOpFlag.Type.STREAM,01>
				<StreamOpFlag.Type.OP,11>
				<StreamOpFlag.Type.TERMINAL_OP,00>
				<StreamOpFlag.Type.UPSTREAM_TERMINAL_OP,00>

STREAM_MASK = (所有的StreaOpFlag的map里面的STREAM的value作或运算)





SORTED(StreamOpFlag): 
	bitPosition: 2
	set: 01 << 2  = 0100
	clear: 10 << 2 = 1000
	preserve: 11 << 2 = 1100
	maskTable: <StreamOpFlag.Type.SPLITERATOR, 0100>
				<StreamOpFlag.Type.STREAM,0100>
				<StreamOpFlag.Type.OP,1100>
				<StreamOpFlag.Type.TERMINAL_OP,0000>
				<StreamOpFlag.Type.UPSTREAM_TERMINAL_OP,0000>

ORDERED(StreamOpFlag): 
	bitPosition: 4
	
SIZED(StreamOpFlag): 
	bitPosition: 6
