This submission tries to have a fixed allocation overhead when using Secure Readers and Writers. All buffers are initialized once at creation and should not need to be expanded (re-allocated) afterwards, based on the behavior of the nacl/box library. This comes at a constant memory cost of the max message size (32KB) for Writer and 3x 32KB for Reader though.