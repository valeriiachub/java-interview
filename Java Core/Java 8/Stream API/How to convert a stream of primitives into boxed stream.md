## How to convert a stream of primitives into boxed stream?
Stream classes which deal with primitives have boxed() method. For example. IntStream#boxed():}

    /**
     * Returns a {@code Stream} consisting of the elements of this stream,
     * each boxed to an {@code Integer}.
     *
     * <p>This is an <a href="package-summary.html#StreamOps">intermediate
     * operation</a>.
     *
     * @return a {@code Stream} consistent of the elements of this stream,
     * each boxed to an {@code Integer}
     */
    Stream<Integer> boxed();

