# SmartScrapy

## Install

    pip install smart_scrapy

## Synopsis

Setting a default value to a Scrapy Field should be as simple as the following:

    import scrapy
    import smart_scrapy
    
    class SomeItem(smart_scrapy.SmartItem):
    
        foo = scrapy.Field(default='something')

With default value:

    >>> some_item = SomeItem()
    >>> print(some_item)
    {'foo': 'something'}

With defined value:

    >>> some_item = SomeItem(foo='bar')
    >>> print(some_item)
    {'foo': 'bar'}

With default value then override:

    >>> some_item = SomeItem()
    >>> print(some_item)
    {'foo': 'something'}
    >>> some_item['foo'] = 'baz'
    >>> print(some_item)
    {'foo': 'baz'}
